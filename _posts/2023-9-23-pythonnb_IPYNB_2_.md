---
toc: True
comments: True
layout: post
title: Python Hack
type: Hacks
courses: {'compsci': {'week': 1}}
---

```python
# Asking name before quiz
name=input("What is your name?")
score = 0
print(f'Hi {name}! Are you ready for the quiz!')
```

    What is your name?drishya
    Hi drishya! Are you ready for the quiz!



```python
#Question 1 sequence
question1=input('Name the Python output command mentioned in this lesson?')
print(f'{question1}')
if question1 == 'print':
    print('Great Job! Ready for the next question?')
    score = score + 1
elif question1=='print()':
        print('Great Job! Ready for the next question?')
        score = score + 1
else:
     print ('Sorry that is incorrect')

```


```python
#Question 2 Sequqnce
question2=input('What is the closest planet to the Sun')
print(f'{question2}')
if question2 == 'Mercury':
    print('Great Job! Ready for the next question?')
    score = score + 1

elif question2 == 'mercury':
    print('Great Job! Ready for the next question?')
    score = score + 1

else:
     print ('Sorry that is incorrect')

```


```python
#score calculation
print(score/2)
```
