# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(john,X):- 
 food(X). 
eats(bill,X):- 
 eats(sue,X). 
eats(Y,X):- 
 food(X). 
eats(bill,peanuts). 
food(apple). 
food(chicken). 
food(peanuts).
```

### Output:
![Screenshot 2023-11-06 132918](https://github.com/Madhav005/AI_Lab_2023-24/assets/110885274/7366bd6b-2463-4de6-9323-bcca9353a0fc)
![Screenshot 2023-11-06 133119](https://github.com/Madhav005/AI_Lab_2023-24/assets/110885274/8700101c-defc-4ec8-924c-b604cca1e867)

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):- 
 easycourse(X). 
hard(sciencecourse). 
easycourse(X):- 
 course(X,dept(havefun)). 
course(bk301,dept(havefun)).
```

### Output:
![image](https://github.com/Madhav005/AI_Lab_2023-24/assets/110885274/8bbee4bd-c4aa-4057-a8b2-9500441c1283)

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
criminal(X):- 
 american(X), 
 weapon(Y), 
 hostile(Z), 
 sells(X,Y,Z). 
weapon(Y):- 
 missile(Y). 
hostile(Z):- 
 enemy(Z,X). 
sells(west,Y,nano):- 
 missile(Y), 
 owns(nano,Y). 
missile(m). 
owns(nano,m). 
enemy(nano,america). 
american(west).
```

### Output:
![image](https://github.com/Madhav005/AI_Lab_2023-24/assets/110885274/26772df7-a8fc-462a-8629-51146b3997ab)

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
