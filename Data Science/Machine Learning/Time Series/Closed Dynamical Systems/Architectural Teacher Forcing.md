---
uni-module: "MBNN"

alias: ["ATF", "Teacherforcing"]
---

# Architectural Teacher Forcing

Similar to [[Error Correction Neural Network|ECNN]] we use this concept to propagate the error from the previous state to the next states. However because we are using only one matrix in [[Historical Consistent Neural Network|HCNNs]] the information gained through it is not lost for future predictions.

![[Bildschirm­foto 2023-05-30 um 14.17.09.png]]

![[Bildschirm­foto 2023-05-30 um 14.17.21.png]]
