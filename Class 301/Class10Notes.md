# In Memory Storage


- Q. What is a ‘call’?


- A. A data structure that uses the LIFO principle to temporarily store and manage function invocation

- Q. How many ‘calls’ can happen at once?


- A. one at a time because it's synchronous

- Q. What does LIFO mean?


- A. Last In First Out

- Q. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.


- A. function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();

- Q. What causes a Stack Overflow?


- A. when there is a recursive function without an exit point.



- Q. What is a ‘reference error’?



- A.  a type of error that occurs in JavaScript when you try to access a variable or function that does not exist or is not currently in scope.


- Q. What is a ‘syntax error’?



- A. a type of error that occurs in programming languages, including JavaScript, when the code violates the language's syntax rules.


- Q. What is a ‘range error’?



- A. a type of error that occurs in JavaScript when a numeric value is not within the valid range of allowed values.


- Q. What is a ‘type error’?



- A. a type of error that occurs in JavaScript when an operation is performed on a value of an inappropriate type.


- Q. What is a breakpoint?



- A. a feature that allows programmers to pause the execution of their code at a specific line or point of interest.


- Q. What does the word ‘debugger’ do in your code?



- A. a JavaScript statement that is used as a debugging tool.