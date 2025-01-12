# Machine Learning Specialization by Coursera Andrew Ng 
I'm currently enrolled in the [Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction#outcomes), which covers a range of foundational machine learning topics.
noting things i learn here.

# other sources i use to keep up with the math 
- https://www.youtube.com/watch?v=fNk_zzaMoSs&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=2     ---> Essence of linear algebra
- https://www.youtube.com/watch?v=WUvTyaaNkzM&list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr&index=2     ---> Essence of calculus

# other sources 
- https://www.youtube.com/watch?v=VMj-3S1tku0 Andrej Karpathy about neural networks


# Generel
- Loss is a measure of the difference of a single example to its target value
- Cost is a measure of the losses over the training set
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

# multiple linear regression

![image](https://github.com/user-attachments/assets/7ee14020-8b31-4c22-a0b6-0443be672796)

 
# Vectorization with python

-numpy 
- fw,b(x) = w (dot) x + b (math)  /////   f = np.dot(w,x) + b (python)
- makes code shorter
- uses paralel hardware

![image](https://github.com/user-attachments/assets/cf9a35ff-1707-47cf-a603-58b216e0a5c6)

![image](https://github.com/user-attachments/assets/58e8d7be-cd42-4f12-b6d4-b495ccd21b2f)



# Gradient descent for multiple regression
-
-

![image](https://github.com/user-attachments/assets/9359cffd-7b07-48f9-a171-a1291b79f50a)



# Notation

![Screenshot 2025-01-07 184731](https://github.com/user-attachments/assets/1f032505-be4c-42e9-be3b-d8e06b3f5457)



# Rescaling features x1 x2 to find a much more direct path to the globa minumum

![image](https://github.com/user-attachments/assets/085309d1-4ceb-475c-b534-c09c39283f48)


# ways to rescale features

![image](https://github.com/user-attachments/assets/2c6214c3-0699-4c30-ab45-b44867e75895)


# Mean normalization
![image](https://github.com/user-attachments/assets/e8b75f0d-c7c9-4476-99e9-1cfe830355bb)


# Z-score normalization
![image](https://github.com/user-attachments/assets/87117da6-0772-4dbf-ab0b-edabb05c793e)

# goals for rescaling 
- aim to get  value from  -1 to +1 for Xj ( for each feature)
- examples
  ![image](https://github.com/user-attachments/assets/358d3325-5202-4adc-9f72-30caac51c77f)

# check if Gradien descent works 
- the cost J should decrease after every single iteration

# choosing the right learning rate
- Learning rate alpha
- if J inscreases even with a small aplha learning rate that means there is a bug somewhere
- picking a really small number for alpha is not good for learning its more a debug step to see if J decreases
- reason is that if learning rate is too small the gradient descent will take a lot of iterations to converge
- increase learning rate by 3Times at a step


![image](https://github.com/user-attachments/assets/41e5c705-2f01-464e-97d4-538300139bba)

![image](https://github.com/user-attachments/assets/b3e96765-5af5-449e-be8c-6441dc3c86c9)


# Logistic regression model
- it inputs  features X and outputs a number between 0 and 1

![image](https://github.com/user-attachments/assets/158ec983-e1f3-4bcf-bb0e-9b6de47331c8)




# sigmoid function also known as logistic function
![image](https://github.com/user-attachments/assets/4ce4eb06-c776-4447-9cae-0096421b2182)
![image](https://github.com/user-attachments/assets/7da08a12-dd15-4114-b249-1409d9455db5)

# sigmoid function in python
def sigmoid(z):
  g = 1/(1+np.exp(-z))

  return g

- exp() is a numpy function to calculate the exponential

# decision boundary
-  w⋅x+b=0
-  if w⋅x+b=0   >0    ===> y= 1
-  if w⋅x+b=0   <0    ===> y= 0

# Logistic regression cost function

![image](https://github.com/user-attachments/assets/7c03e72f-158f-4a57-8deb-4b4d641e6968)



# gradient descent for logistic regression
- at first it look smiliar to the normal linear regression but this time the f(x) function changed see picture
- ![image](https://github.com/user-attachments/assets/9e6c7e26-90a6-4ef9-a405-11a3f309585c)

# algorithm can be underfit, just right, overfit
- goal is to generalize well so it predicts good even with brand new examples
- overfit  ---> doing very well on the training data but will do poorly on new examples   (too many features) fix: 1 option is to get more data or use fewer features or reduze size of parameters instead of removing them 
- underfit ---> not enough features

# regularization term
- if lambda is very large it will end up in a horizontal straight line and underfits
- if lamda 0 ---> overfit
![image](https://github.com/user-attachments/assets/e2212c1c-c904-4a49-b691-c3147d999de4)
