---
uni-module: "InfoVis"
---

# Walker's Algorithm

Used to determine layout of [[Hierarchy]].

```js
/** compute left contour of tree */
function leftContour(node, modSum, lcMap) {
  const key = node.data.y;
  if (!lcMap.has(key)) {
    lcMap.set(key, node.data.x + modSum);
  } else {
    const xVal = Math.min(lcMap.get(key), node.data.x + modSum);
    lcMap.set(key, xVal);
  }
  modSum += node.data.mod;
  if (hasChildren(node)) {
    node.children.forEach((c) => leftContour(c, modSum, lcMap));
  }
}
/** compute right contour of tree */
function rightContour(node, modSum, rcMap) {
  const key = node.data.y;
  if (!rcMap.has(key)) {
    rcMap.set(key, node.data.x + modSum);
  } else {
    const xVal = Math.max(rcMap.get(key), node.data.x + modSum);
    rcMap.set(key, xVal);
  }
  modSum += node.data.mod;
  if (hasChildren(node)) {
    node.children.forEach((c) => rightContour(c, modSum, rcMap));
  }
}
/** center smaller trees in-between sibling */
function centerSiblings(lNode, rNode) {
  const lIndex = lNode.parent.children.indexOf(lNode);
  const rIndex = rNode.parent.children.indexOf(rNode);
  const nrNodes = rIndex - lIndex - 1;
  if (nrNodes > 0) {
    // there is at least one node in-between
    var stepSize = (rNode.data.x - lNode.data.x) / (nrNodes + 1);
    let count = 1;
    for (let i = lIndex + 1; i < rIndex; i++) {
      const mNode = lNode.parent.children[i];
      const targetX = lNode.data.x + stepSize * count;
      const offset = targetX - mNode.data.x;
      mNode.data.x += offset;
      mNode.data.mod += offset;

      count++;
    }
  }
}
/** solve subtrees overlap by checking for collision of left with right contours */
function contourCollision(node) {
  let maxShift = 0;
  let distance = treeDistance + nodeSize;
  const lcMap = new Map();
  leftContour(node, 0, lcMap);
  const siblings = allLeftSiblings(node);
  let cNode = undefined;
  for (let s of siblings) {
    let shift = 0;
    const rcMap = new Map();
    rightContour(s, 0, rcMap);
    const minDepth = node.data.y + 1;
    const maxDepth = node.data.y + Math.max(lcMap.size, rcMap.size) - 1;
    for (let depth = minDepth; depth <= maxDepth; depth++) {
      if (lcMap.has(depth) && rcMap.has(depth)) {
        let d = lcMap.get(depth) - rcMap.get(depth);
        if (d + shift < distance) {
          shift = distance - d;
        }
      }
    }
    if (shift > 0) {
      if (maxShift < shift) {
        maxShift = shift;
        cNode = s;
      }
    }
  }
  // update position
  node.data.x += maxShift;
  node.data.mod += maxShift;
  // center smaller subtrees
  if (cNode !== undefined) {
    centerSiblings(cNode, node);
  }
}
/** move tree if nodes are outside the scree - check only left contour or root node */
function nodesOnScreen(node) {
  const lcMap = new Map();
  leftContour(node, 0, lcMap);
  let shift = 0;
  lcMap.forEach((v) => {
    if (v + shift < 0) {
      shift = -v;
    }
  });
  if (shift > 0) {
    node.data.x += shift;
    node.mod += shift;
  }
}
/** compute node's initial position - postorder tree traversal */
function initialX(node) {
  if (hasChildren(node)) {
    node.children.forEach((c) => {
      initialX(c);
    });
  }
  if (isLeaf(node)) {
    if (!isLeftMost(node)) {
      node.data.x = previousSibling(node).data.x + nodeSize + siblingPadding;
    } else {
      node.data.x = 0;
    }
  } else if (node.children.length === 1) {
    if (isLeftMost(node)) {
      node.data.x = node.children[0].data.x;
    } else {
      node.data.x = previousSibling(node).data.x + nodeSize + siblingPadding;
      node.data.mod = node.data.x - node.children[0].data.x;
    }
  } else {
    const leftChild = leftMostChild(node);
    const rightChild = rightMostChild(node);
    const midpoint = (leftChild.data.x + rightChild.data.x) / 2;
    if (isLeftMost(node)) {
      node.data.x = midpoint;
    } else {
      node.data.x = previousSibling(node).data.x + nodeSize + siblingPadding;
      node.data.mod = node.data.x - midpoint;
    }
  }

  if (hasChildren(node) && !isLeftMost(node)) {
    contourCollision(node);
  }
}
/** compute node's final position - preorder tree traversal */
function finalPosition(node, modSum, bbox) {
  node.data.x += modSum;
  modSum += node.data.mod;
  if (hasChildren(node)) {
    node.children.forEach((c) => {
      finalPosition(c, modSum, bbox);
    });
  }
  const x = node.data.x;
  const y = node.data.y;
  if (x < bbox.xmin) bbox.xmin = x;
  if (x > bbox.xmax) bbox.xmax = x;
  if (y < bbox.ymin) bbox.ymin = y;
  if (y > bbox.ymax) bbox.ymax = y;
}
/** initialize node - preorder tree traversal */
function initPosition(node) {
  node.data.x = -1;
  node.data.y = node.depth;
  node.data.mod = 0;
  if (hasChildren(node)) {
    node.children.forEach((c) => {
      initPosition(c);
    });
  }
}
```
