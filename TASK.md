Task Description
Consider the following Bayesian Network
![image](https://github.com/user-attachments/assets/f6a4f6dc-b017-4411-affc-d50ab470b99f)
Image 1: A Bayesian Network

The Variables used here are as followes
B : True if there is a Baseball Game on TV, False if not
G: True if George watches TV, False if not
C: True if George is out of Cat Food, False if not
F: True if George feeds his cat, False if not.

Let us say you are given some Training Data which represents what happens over a period of time (For example: This file contains what happens every evening over one specific year). Your Task is to learn the conditonal probabilty tables for the bayesian network from the training data. The training data will be formatted as follows:
The first number is 0 if there is no baseball game on TV (B is false), and 1 if there is a baseball game on TV (B is true).
The second number is 0 if George does not watch TV (G is false), and 1 if George watches TV (G is true).
The third number is 0 if George is not out of cat food (C is false), and 1 if George is out of cat food (C is true).
The fourth number is 0 if George does not feed the cat (F is false), and 1 if George feeds the cat (F is true).

Your program should be called bnet and the command line invocation should follow the following format:

bnet.py <training_data>
<training_data> text file with training data.

Once you are done calculating the conditional probabilites, the program should calculate the probabilty for any event given evidence (if available) using inference by enumeration.

Your program should display a prompt 'Query:' where you can enter the query in the following format

 Query: <query variable values> [given <evidence variable values>]
 Values of Query Variables using the following format
 Bt if B is true, Bf if B is false
 Gt if G is true, Gf if G is false
 Ct if C is true, Cf if C is false
 Ft if F is true, Ff if F is false
 Values of Evidence Variable (if any) [Format is same as for Query Variable]
 Sample Queries:
 Query: Bt Gf given Ff  will use the Bayesian Network to calculate P(B=t, G=f | F=f)
 Query: Bt Ff  will use the Bayesian Network to calculate P(B=t, F=f)
 You can display the calculated probabilty values in standard output.
 After displaying the calculated probabilty, request another Query by displaying the prompt.
 Repeat till Query is given as None.
 Query: None will exit the program

Note: You may want to write a function in your code that uses the semantic forumla for bayesian network to reconstruct the JPD values from the Bayesian Network values that you have calculated. You can use this function to obtain the JPD values when performing Inference by enumeration.
