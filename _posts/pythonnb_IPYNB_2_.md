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
