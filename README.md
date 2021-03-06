#TDD kata stringcalc

A java starter project for the stringcalculator TDD kata as created by [Roy Osherove](https://osherove.com/home).

https://osherove.com/tdd-kata-1

All the dependencies are configured (jUnit5 and Hamcrest)
Begin your daily 30 minutes TDD using it as the start point.

Hints:
- Start with the simplest test case of an empty string and move to one and two numbers
- Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
- Remember to refactor after each passing test

#Stories

## 1.Stringcalc 
* Create a simple String calculator with a method signature:
```
int Add(string numbers)
```
* returns sum of 2 numbers
* comma separated
* empty string returns 0

## 2. Allow the method to handle an unknown amount of numbers
* Allow the Add method to handle new lines between numbers (instead of commas).
* Correct input: `“1\n2,3”` Result is 6
* Incorrect input: `“1,\n”` (not need to prove it - just clarifying)

## 3. Support different delimiters
* to change a delimiter, the beginning of the string will contain a separate line that looks like this: 
```  
“//[delimiter]\n[numbers…]”
```
for example `“//;\n1;2”` should return 3
* the first line is optional.
* all existing scenarios should still be supported

## 4. Negative numbers
*  Calling Add with a negative number will throw an exception “negatives not allowed” - and the negative that was passed. 
* if there are multiple negatives, show all of them in the exception message.


#STOP HERE! Only continue if you can finish the steps so far in less than 30 minutes.

---

## 5. Numbers bigger than 1000
* should be ignored, so adding 2 + 1001 = 2

## 6. More Delimiters
* can be of any length with the following format:
```  
“//[delimiter]\n”
```
for example: `“//[***]\n1***2***3”` should return 6

## 7. Allow multiple delimiters like this: 
```   
“//[delim1][delim2]\n”
 ```
for example `“//[*][%]\n1*2%3”` should return 6.
* make sure you can also handle multiple delimiters with length longer than one char