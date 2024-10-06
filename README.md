# Machine Learning Specialization by Coursera Andrew Ng 
I'm currently enrolled in the [Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction#outcomes), which covers a range of foundational machine learning topics.
noting things i learn here.


- supervised Learning ---> gives the learning algorithm examples to learn on with correct answers   -->  input x to output y
  - types = Regression leanrs to predict number out of infinite possible numbers
          = Classification predict categories dont have to be numbers for example pictures small limited set of possible output categories like 0 and 1 and so on


    - Regression Models: Linear regression = has right answers 
    classification models predicting categories small number of possible output 

- unsupervised Learning ---> finding structures Clustering groups categories without giving any output y only with the input x

-training set ==>  (x(i), y(i))= i th the (i) is the index nothing else in the training set contains features and targets 

Linear regression
f w,b(x) = wx + b
f(x) = wx + b short form
Univariate = 1 variable 

![Screenshot 2024-10-03 173006](https://github.com/user-attachments/assets/3560bbbb-90cd-42ab-9311-08d6105e3262)


w value = the Slope (Steigung)
![image](https://github.com/user-attachments/assets/60b67bcb-7d76-4428-989f-c38917220691)


- Cost Function
- The cost is a measure of how accurate the model is on the training data.
- measures the difference between the models predictions and the actual values

- ![image](https://github.com/user-attachments/assets/5d5efcac-f1da-45ab-8907-7ac733f3941c)

- simplified version
- b is set to 0


- each value of w will point to a single point to the J(w)
- for example if w = 1 u can see the fw(x) line on the left that will point to a single point on the graph of  J(w) on the right
![image](https://github.com/user-attachments/assets/03ef9bb0-2202-48e2-aeaa-04bdde6dacec)

- goal of linear regression minimize J(w)
- genreal case minimize J(w,b)
- The goal of linear regression is to find the parameters w or w and b that results in the smallest possible value for the cost function J
![image](https://github.com/user-attachments/assets/15296142-e479-4e9a-81c1-b6a6b1753927)

-visualize cost function 
- u can visualize the 3d plot also as a 2d contour plot

- gradient descent algorithm
- start with  (w =0, b=0)
- keep changing w,b to reduce j(w.b) to a minimum
- it is possible for there to be more than one possible minimum
- update Simultaneous
- the alpa symbol is the learning rate (The learning rate controls how big of a step you take when updating the model's parameters, w and b)
- if alpha the learning rate is too small it the gradient decent will work but it may be slow !
- if alpha is too large  gradient decent may overshoot and never reach the minimum
- if the values starts at the minumum the gradient decent steps will do nothing it keeps the solution at the local minimum
- can reach local minum with fixed learning rate alpha
- near a local minumum the derivate becomes smaller that means the update steps will also get smaller
- convex function is bowl shaped and can only have one global minumum
- batch gradient descent  batch because each step of gradient descent uses all the training examples
- ![image](https://github.com/user-attachments/assets/555bd699-d096-4e50-86e2-63d048fc30df)

  
