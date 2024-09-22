  ###### Reference Link:
https://www.geeksforgeeks.org/arrays-in-java/?ref=lbp#basics-of-arrays-in-java

## Arrays in Java
- **Arrays** are fundamental structures in Java that allow us to store multiple values of the same type in a single variable. 
- They are useful for managing collections of data efficiently.
#### Array Declaration
- To declare an array in Java, use the following syntax:

`type[] arrayName;`

- **type**: The data type of the array elements (e.g., `int`, `String`).
- **arrayName**: The name of the array.

##### Example
```java
int[] numbers; // declaring an integer array 
```

#### Create an array
To create an array, you need to allocate memory for it using the new keyword.

numbers = new int[5]; // Creating an array of 5 integers

- This statement initializes the `numbers` array to hold 5 integers. The default value for each element is `0`.
```java
numbers[0] = 10; // Setting the first element of the array
int firstElement = numbers[0]; // Accessing the first element
```

##### Array length

```java
int length = numbers.length; // Getting the length of the array
```