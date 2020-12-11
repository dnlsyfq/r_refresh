### Data Types
* Vectors: A list of related data that is all the same type.
* Logical : TRUE | FALSE 
* NA : absence of a value, and is represented by the keyword NA (without quotes)

```
class(var)
```

### Vector 
* contains elements of the same type, whether they’re numericals, doubles, characters, logical (TRUE or FALSE), or complex numbers
* one-dimensional
* create vectors using the function c()
* sequential
* look up the ith element of a vector v by calling v[i]
* select multiple elements by specifying indices in a vector
# select third and fifth element
    example_vector[c(3, 5)]
# selects the first four elements of the vector
    example_vector[c(1:4)]   
    
    
```
spring_months <- c("March", "April","May","June")
one_thru_ten <- c(1:10)


example_vector <- c("I", "have", "several", "items", "inside", "me") 
example_vector[1] # gets the first element "I"
example_vector[3] # gets the third element "several"
```

* typeof(vector_name)
* length(vector_name)
* slicing:
  vector_name[2]
* typeof(vector_name)

* modify element
```
change_me <- c(7, 11, -28, 32, 5, 19)
# sets second element to 7
change_me[2] <- 7


change_me <- c(7, 11, -28, 32, 5)
# set elements in vector greater than 0 AND less than 10 to 0
change_me[change_me > 0 & change_me < 10] <- 0

change_me <- c(7, 11, -28, 32, 5)
# Cut the vector to the portion containing second to the fourth element
change_me <- change_me[2:4]
```

### Matrix 
A matrix (plural: matrices) is a 2-D data structure that holds elements of the same type

matrix() function to specify what the matrix should contain, and how many rows and columns it should have. The matrix() function takes three arguments

* The first argument should be data you’d like to keep in the matrix. If we specify just one value, the entire matrix will be filled with it. If we specify a vector, R will determine whether it should repeat throughout the matrix or if it fills the whole matrix, depending on the vector’s length. The vector’s data is inserted column-wise by default.
* nrow = number of rows
* ncol = number of columns

```
different_neighbors <- matrix(
  c(1,0,1,0,1,0,1,0,1,0,1,0,1,0,1),nrow=3,ncol=5
)

zeros <- matrix(0,nrow=2,ncol=2)
```

* find the element at the xth row, yth column using my_matrix[x,y]
```
my_matrix <- matrix(c(1:25), nrow = 5, ncol = 5) # col-wise

# select the element in the second row, third column (position in the row)
my_matrix[2, 3]

# select the entire second row as a vector
my_matrix[2, ]

#select the entire third column as a vector
my_matrix[, 3]



```
### List 

can contain multiple data types, unlike vectors. They can also store lists, meaning there can be lists of lists… of lists.
```
my_list <- list(a, b, c) where a, b, c could be different data types.
```

To access items in a list in R by their position, we can call the index we want in double brackets
```
third_item <- my_list[[3]]
```

Modifying elements is also straightforward.
```
my_list[[3]] <- 85.2
```

```

# create list fruit_basket below:
fruit_basket <- list('mangoes',5,c('Lila','Mim'))

# print the list
fruit_basket[[2]] <- 10
print(fruit_basket)

```

to create a list with named items inside is my_list <- list(name1 = a, name2 = b, name3 = b)

```
# a list that has three vectors named Penny, Xavier, and Kiara
test_scores <- list(Penny = c(84, 79, 85), Xavier = c(89, 90, 82), Kiara = c(92, 89, 87))

# get Penny's test scores (vector)
penny_scores <- test_scores$Penny
print(penny_scores)

# a list that has three vectors named Penny, Xavier, and Kiara with the name of each exam inside the vectors
test_scores <- list(
  Penny = list(exam1 = 84, exam2 = 79, exam3 = 85),
  Nick = list(exam1= 77, exam2 = 81, exam3 = 83),
  Kiara = list(exam1 = 92, exam2 = 89, exam3 = 87)
)


```

### Data Frame

```
student_scores <- data.frame(
    student = c("Penny", "Xavier", "Kiara"), 
    exam1 = c(84, 77, 92),
    exam2 = c(79, 81, 89),
    exam3 = c(85, 83, 87),
    extra_credit = c(TRUE, TRUE, FALSE)
)

print(student_scores$extra_credit)
# output: [1] TRUE TRUE FALSE
```



  
### Conditionals

```
if (TRUE) {
   print("Go to sleep!")
} else {
   print("Wake up!")
}
```

### Operators 


```
Less than: <
Greater than: >
Less than or equal to: <=
Greater than or equal to: >=
Is equal to: ==
Is NOT equal to: !=
```

### Logical operators 

```
the AND operator (&)
the OR operator (|)
the NOT operator, otherwise known as the bang operator (!)
```

```
if (stopLight == 'green' & pedestrians == 0) {
  print('Go!');
} else {
  print('Stop');
}
```

### function

```
sort(c(2,4,10,5,1)); # Outputs c(1,2,4,5,10)
length(c(2,4,10,5,1)); # Outputs 5
sum(5,15,10) #Outputs 30
```
* sqrt(var)
* floor(var)
* ceiling(var)
* unique(var)

### packages

```
install.packages('package-name')
library(package-name)
```

### data analysis and statistical computing 

dplyr

* statistical model
```
fit <- lm(dist~speed,data=cars)
```

* vectorized calculations
```
x <- 1:10

x_squared = c()

for(i in 1:length(x)){
  x_squared[i] = x[i]**2
}

x_squared <- x ** 2
```

* data viz 

```
ggplot(iris, aes(x=Sepal.Length, y=Petal.Length, color=Species)) +
  geom_point() + 
  labs(x='Sepal Length',y='Petal Length')
```



