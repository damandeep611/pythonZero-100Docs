---
title: Functions and modules
sidebar_position: 2
---

# Functions and Modules in Python

Whenever we are making a program or a application, it contains a lot of small tasks / specific tasks that are sometimes reused in the program. if we have to write those tasks without any identification mark, then we would not be able to debug the errors easily and also we would not be able to make the application function properly because the code will not be properly written, that's why we use functions, 

Functions help us encapsulate these small specific tasks that we can reuse again in the program. for example : - 

- the following function prints the name of the user with the greetings, so we will warp it in a function and define it with appropriate name, so that we can easily locate it when ever we will need to reuse it later, defining functions with appropriate name is the most important thing , 
``` python 
def say_hello(name):
  print(f"Hey {name}, say hello to the flash")
```


## Modules 
Modules are just functions, variables and classes that we import outside the working file, as we would import certain pre build functions from outside the directory, or program file. Modules are simply files that contains readymade functions, variables and classes.
- it provides better reuseabilty and organization 

There are three types of modules 
1. Build in modules - in build python functions 
2. Third Party - Imported / installed using pip
3. User defined local modules  
