### Data Types
* Vectors: A list of related data that is all the same type.
* Logical : TRUE | FALSE 
* NA : absence of a value, and is represented by the keyword NA (without quotes)

```
class(var)
```

### Vector 

```
spring_months <- c("March", "April","May","June")
```

* typeof(vector_name)
* length(vector_name)
* slicing:
  vector_name[2]
  
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



