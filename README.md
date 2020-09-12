## Probability and Combinatorics



```python
import math
```

### 1. Set Theory

Given the following probabilities:

$P(A) = 0.7$

$P(B) = 0.5$

$P(B|A) = 0.4$

Calculate the following probabilities. Write an explanation of your logic in comments or as a multiline string. 

Rather than "hard-coding" an answer, show your work by adding/subtracting/multiplying/dividing the original probabilities, e.g. `0.2*0.1` rather than just writing `0.02`

Hint: draw a diagram if you're getting stuck!

#### Question 1: $P(A and B)$
    
Assign your answer to the variable `ans1`


```python
ans1 = None
### BEGIN SOLUTION

from test_scripts.test_class import Test
test = Test()

"""
Question 1:

We use the conditional probability formula: P(B|A) = P(A and B)/P(A)
P(A and B) = P(B|A)*P(A) = 0.4*0.7 = 0.28
"""

a = 0.7
b_given_a = 0.4
ans1 = b_given_a * a

test.save(ans1, "ans1")


### END SOLUTION
ans1
```




    0.27999999999999997




```python
# PUT ALL WORK FOR THE ABOVE QUESTION ABOVE THIS CELL
# THIS UNALTERABLE CELL CONTAINS HIDDEN TESTS

# ans1 should be a floating point probability between 0 and 1
assert type(ans1) == float

### BEGIN HIDDEN TESTS

from test_scripts.test_class import Test
test = Test()

test.run_test(ans1, "ans1")


### END HIDDEN TESTS
```

#### Question 2: $P(A|B)$
    
Assign your answer to the variable `ans2`


```python
ans2 = None
### BEGIN SOLUTION

from test_scripts.test_class import Test
test = Test()


"""
Question 2:

P(A|B) = P(A and B)/P(B) = 0.28/0.5 = 0.56
"""
b = 0.5
ans2 = ans1/b

test.save(ans2, "ans2")

### END SOLUTION
ans2
```




    0.5599999999999999




```python
# PUT ALL WORK FOR THE ABOVE QUESTION ABOVE THIS CELL
# THIS UNALTERABLE CELL CONTAINS HIDDEN TESTS

# ans2 should be a floating point probability between 0 and 1
assert type(ans2) == float

### BEGIN HIDDEN TESTS

from test_scripts.test_class import Test
test = Test()

test.run_test(ans2, "ans2")

### END HIDDEN TESTS
```

#### Question 3: True or false: $P(A or B)$ is always equal to $P(A)$ + $P(B)$. Explain your answer

False. This is only true for _disjoint_ events, where there is no possibility that A and B can happen at the same time. If A and B can happen at the same time, you are "double-counting" if you just add P(A) to P(B)

### 2. Card Combinatorics

A standard deck of playing cards consists of 52 cards in each of the four suits of spades, hearts, diamonds, and clubs. Each suit contains 13 cards: Ace, 2, 3, 4, 5, 6, 7, 8, 9, 10, Jack, Queen, and King.
    
You have a standard deck of 52 cards and are asked the following questions:

Answer the questions below:

#### Question 4: What is the probability of drawing a King or a Queen?

Assign your answer to the variable `ans4`


```python
ans4 = None
### BEGIN SOLUTION

from test_scripts.test_class import Test
test = Test()

"""
Question 4:

P(King or Queen) = Number of Kings + Queens / Total Number of Cards = 8/52 = 2/13
"""
ans4 = 2/13

test.save(ans4, "ans4")

### END SOLUTION
ans4
```




    0.15384615384615385




```python
# PUT ALL WORK FOR THE ABOVE QUESTION ABOVE THIS CELL
# THIS UNALTERABLE CELL CONTAINS HIDDEN TESTS

# ans4 should be a floating point probability between 0 and 1
assert type(ans4) == float

### BEGIN HIDDEN TESTS

from test_scripts.test_class import Test
test = Test()

test.run_test(ans4, "ans4")

### END HIDDEN TESTS
```

#### Question 5: How many possible 5-card combinations can be formed with this deck of 52 cards?

Assign your answer to the variable `ans5`


```python
ans5 = None
### BEGIN SOLUTION


from test_scripts.test_class import Test
test = Test()

"""
Question 5:

Number of 5-card combinations = Number of ways to choose 5 from 52 = 52!/(5!*47!) = 2598960
"""
ans5 = math.factorial(52)/(math.factorial(5) * math.factorial(47))

test.save(ans5, "ans5")

### END SOLUTION
ans5
```




    2598960.0




```python
# PUT ALL WORK FOR THE ABOVE QUESTION ABOVE THIS CELL
# THIS UNALTERABLE CELL CONTAINS HIDDEN TESTS

# ans5 should be a number greater than 1
assert type(ans5) == int or type(ans5) == float

### BEGIN HIDDEN TESTS

from test_scripts.test_class import Test
test = Test()

test.run_test(ans5, "ans5")

### END HIDDEN TESTS
```
