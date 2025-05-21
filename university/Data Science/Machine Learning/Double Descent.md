# Double Descent

Reference: [[Double descent in human learning · Chris Said.pdf]]

Phenomenon where increasing the **number of model parameters**, **training the model longer** or **increasing the number of training samples** causes the test performance to get better, then worse, and then better again.

So it first [[Underfitting|underfits]], then [[Overfitting|overfits]] and then generalizes quite well.

We can think of the classical regime ([[Bias]] vs [[Varianz|Variance]]) and the modern regime where the model can generalize really well.

![[Bildschirmfoto 2023-07-08 um 14.14.33.png]]
Example for [[Linear Regression]] with polynomial basis functions

![[Bildschirmfoto 2023-07-08 um 14.16.20.png]]
![[Bildschirmfoto 2023-07-08 um 14.18.59.png]]


So at the transition point between an **underparameterized regime** to an **overparameterized regime** we get an explosion of the test error as you can see from the above plots.

Also see: [[U-shaped Learning]]