---
toc: true
comments: true
layout: post
title: Python Hacks
description: Python IO
type: hacks
courses: { compsci: {week: 1} }
---


```python
#Question 1 sequence
question1=input('Name the Python output command mentioned in this lesson?')
print(f'{question1}')
if question1 == 'print':
    print('Great Job! Prepare for the next question.')
    score = score + 1
elif question1=='print()':
        print('Great Job! Prepare for the next question.')
        score = score + 1
else:
     print ('Sorry that is incorrect. Prepare for the next question.')

```


```python
#Question 2 Sequqnce
question2=input('What is the closest planet to the Sun')
print(f'{question2}')
if question2 == 'Mercury':
    print('Great Job! Prepare for the next question.')
    score = score + 1

elif question2 == 'mercury':
    print('Great Job! Prepare for the next question.')
    score = score + 1

else:
     print ('Sorry that is incorrect. Prepare for the next question.')

```

```python 
#Question 3 Sequence
question3=input('What is the largest planet in the solar system')
print(f'{question3}')
if question3 == 'Jupiter':
    print('Great Job! Your score will now be calculated.')
    score = score + 1

elif question3 == 'jupiter'
    print('Great Job! Your score will now be calculated.')
    score = score + 1

else:
    print('Sorry that is incorrect, your score will now be calculated.')


```


```python
#score calculation
input("Press any button to see your score.")
print("You scored " + score/3)
```
