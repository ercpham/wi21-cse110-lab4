## Variables and Scoping

### Using `var`

1. What will happen at line 11 and why?

    It returns the value of `i` at the end of the loop because it is still in scope after the loop is done.

2. What will happen at line 12 and why?

    It returns the value of `discountedPrice` in the final iteration of the loop because the function scope is not closed after the loop.

3. What will happen at line 13 and why?

    It returns the final price of the last item in the discounted array because final price is last defined in the final iteration of the loop, and the scope is still in the function.

### Using `let`

4. What will the function return if we call discountPrices([100, 200, 300], .5) ? Give a brief explanation.

    The function will return a list: [50, 100, 150]. The function applies a discount and rounds the number to the ones place.

5. What will happen at line 11 and why?

    There will be an error, as `i` is no longer in scope outside the loop.

6. What will happen at line 12 and why?

    There will be an error, as `discountedPrice` is no longer in scope outside the for loop.

7. What will happen at line 13 and why?

    It returns the value of `finalPrice` in the last iteration of the loop. It is still in scope because it is in the same block.

### Using `const`

8. What will the function return if we call discountPrices([100, 200, 300], .5) ? Give a brief explanation.

    The function will return a list: [50, 100, 150]. The function applies a discount and rounds the number to the ones place. This is the same as #4 because the variable scoping does not affect functionality. 

9. What will happen at line 11 and why?

    There will be an error because `i` is not in scope anymore.

10. What will happen at line 12 and why?

    There will be an error because `discountedPrice` will not be in scope anymore.

11. What will happen at line 13 and why?

    You won't be able to assign the variable in the code, but if there was not an error, the finalPrice should remain zero because it is a const, and it is still in scope.

12. What will the function return for discountPrices([100, 200, 300], .5)? Give a brief explanation.

    The function will not return because you are trying to assign a different value to a const variable. 

## Data Types
13. Given the above Object, write the notation for

    A. Accessing the value of the name property in the student object
    
    `student['name']`

    B. Accessing the value of the Grad Year property in the student object

    `student['Grad Year']`

    C. Calling the function for the greeting property in the student object

    `student['greeting']`

    D. Accessing the name property of the object in the Favorite Teacher property in student

    `student['Favorite teacher']['name']`

    E. Access the first index in the array of the courseLoad property of the student object 

    `student['courseLoad'][1]`

## Basic Operators & Type Conversion
14. Arithmetic

    A. `'3' + 2`

    `"32"`: A number added to a string will append the number as a string to create a larger string

    B. `'3' - 2`

    `1`: Because `-` is not a string operation, JS will automatically do numeric conversion and a number will be returned

    C. `3 + null`

    `3`: In numeric conversion, `null` is 0.

    D. `'3' + null`

    `"3null"`: When adding null to a string, `null` is treated as a string as well and it is appended to the string

    E. `true + 3` 

    `4`: When adding a boolean and a number, the booleans are treated as numbers, with true corresponding to 1. 

    F. `false + null`

    `0`: False and null both correspond to the number `0`, so adding them will result in `0`

    G. `"3" + undefined`

    `"3undefined"`: The plus operator is seen as a string append, so undefined will simply be appended to the string 3.

    H. `"3" - undefined`

    `NaN`: JS sees a minus operator and tries to do number conversion to do math. However, `undefined` corresponds to `NaN`, and when you try to do math with `NaN`, the output is `NaN`

15. Comparison

    A. `'2' > 1`

    `true`: When comparing different types, JS converts both to numbers and 2 is indeed greater than 1

    B. `'2' < '12'`

    `false`: When comparing two strings, the lexographic order is compared, and `'2'` comes after `'1'` in order, so this statement is false.

    C. `2 == '2'`

    `true`: When comparing different types with `==`, both sides are converted to numbers and compared, and 2 is indeed equal to 2. 

    D. `2 === '2'`

    `false`: The `===` operator compares both the type and the value, and because these are of different types, this will return false.

    E. `true == 2`

    `false`: true is converted to 1 in the comparison, and 1 is not equal to 2. 

    F. `true === Boolean(2)`

    `true`: The explicit conversion of 2 to a boolean will make it true, and because both sides are of the same value and type, this will return true.

16. Explain the difference between the == and === operators.

    The `==` operator compares only the values, allowing for type conversion. The `===` operator compares values and types, so two items of different types will never be equal.

17. From the code snippet, explain what gets printed and why.

    `'How are you'` is printed. The first condition is false because `true` is converted to `1` and 2 is not equal to 1. However, in the second condition, `2` is converted to `true`, so the code block executes. The else condition is not reached. 

18. See part1-question18.js file

19. If the function below is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result.

    1. For each element in the given array, we push a modified value into the new array
    2. What is that value? The value will be the return value of `doSomething`, a function that accepts a number and a function as parameters.
    3. In doSomething, our arguments are the value of the old array at a given index, and a function that returns 2 times a given parameter.
    4. In doSomething, the function will be called with an argument of the array entry plus 2. Therefore, each number in the new array will be two times the sum of the old number and 2. 
    5. Our result is [6, 8, 10]

20. see part1-question20.js

21. What is the output of the code?

```
1
4
3
2
```