This is especially helpful when you forgot to create a release on GitHub.


Set the HEAD to the old commit that we want to tag
```
git checkout <hash>
```

Temporarily set the date to the date of the HEAD commit, and add the tag
```
GIT_COMMITTER_DATE="$(git show --format=%aD | head -1)" \
git tag v1.2 <hash>
```

Push to origin
```
git push origin --tags
```

Set HEAD back to whatever you want it to be
```
git checkout master
```

