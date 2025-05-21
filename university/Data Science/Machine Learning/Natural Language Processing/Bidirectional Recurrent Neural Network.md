---
uni-module: AI
aliases:
  - Bidirectional RNN
---
# Bidirectional Recurrent Neural Network

Concatenation of a right-to-left [[Recurrent Neural Network|RNN]] onto a left-to-right [[Recurrent Neural Network|RNN]].

## Example Architecture

Example [[POS Tagging]].

For this example the bidirectionality ensures that the network at the word *cut* will get information of the words context both from the prefix and postfix. 

![[CleanShot 2023-10-03 at 22.03.42@2x.png]]