---
toc: true
comments: true
layout: post
title: Collegeboard Review quiz
courses: {'compsci': {'week': 26} }
type: tangibles
---


### q 41

<iframe src="https://drive.google.com/file/d/1qWBrbTLZljZGYxSM1fJPJKNab0LG3PdC/preview" width="640" height="480" allow="autoplay"></iframe>

Why the Wrong Answers Are Wrong:

B: Turning chat off doesn't involve the community. It's just a setting change.
C: Software doing the monitoring is about technology, not people helping out.
D: Updating rules and making people sign them is a company action, not asking players to help.

Correct Answer:
A: This option is about players giving thumbs-up to other nice players. It's using the crowd (all the players) to find and reward the good ones. When enough players say someone is great, that person gets a gift in the game. This is what crowdsourcing is all about: getting everyone to chip in.

### q 43

<iframe src="https://drive.google.com/file/d/1USb62QnQ9DjcNeQzN3b5bH5_Z3Rxgedm/preview" width="640" height="480" allow="autoplay"></iframe>

Why the Wrong Answers Are Wrong:

B: Guessing a common password is just trial and error. No special tool like keylogging is used.
C: Watching data on an unsecure website is about intercepting, not recording keystrokes.
D: This is phishing, tricking you into giving away your info, not keylogging.

Correct Answer:
A: This one's about a sneaky program that records what you type, like passwords, and sends it to someone else. That's exactly what keylogging does: track and send your keystrokes to someone who shouldn't have them.

### q 47

<iframe src="https://drive.google.com/file/d/1tyz64754OaHAAi1KxnvQxNDJGpIkaYCC/preview" width="640" height="480" allow="autoplay"></iframe>

Option A: This will filter for restaurants with an average rating greater than or equal to 4.0 AND a price range of "lo" AND a price range of "med". This is impossible because a restaurant cannot have both "lo" and "med" as its price range simultaneously, hence it's incorrect.

Option C: This will filter for restaurants with an average rating greater than or equal to 4.0 OR a price range of "lo" AND NOT "med". This is incorrect because it would include all restaurants with high ratings regardless of price and all low-cost restaurants regardless of rating.

Option D: This will filter for restaurants with an average rating greater than or equal to 4.0 OR a price range of "lo" OR a price range of "med". This is incorrect because it would include all restaurants with high ratings, all low-cost restaurants, and all medium-cost restaurants, regardless of their rating.


Correct Answer: 
Option B: This will filter for restaurants with an average rating greater than or equal to 4.0 AND a price range of either "lo" OR "med". This is the correct logic because it allows for restaurants in either the "lo" or "med" price range, not both at the same time.

### q 49

<iframe src="https://drive.google.com/file/d/1tIxt9knNQM3mI5oDlpdXgDYbOHOXmd-y/preview" width="640" height="480" allow="autoplay"></iframe>

Why the Wrong Answers Are Wrong:

A: While human validation may be necessary for some outputs, this doesn't explain the core concept that some problems inherently cannot be solved by any algorithm.
B: Using multiple devices in parallel can speed up processing but doesn't affect whether a problem can be algorithmically solved at its core.
C: The amount of data storage available doesn't determine the solvability of a problem algorithmically. It might affect performance or feasibility but not the fundamental ability to solve a problem.

Correct Answer: 
D is correct because there are indeed some problems that can't be solved by any algorithm. This is a fundamental principle in computer science related to computability theory. Some problems are undecidable, meaning no algorithm can be written to solve them for all possible inputs.

### q 51

<iframe src="https://drive.google.com/file/d/10aAM_32zPpHZNM61um2LMtpy4uhsQ6vo/preview" width="640" height="480" allow="autoplay"></iframe>

Why the Wrong Answers Are Wrong:

B: Monitoring cell growth in a lab requires controlled conditions and specialized equipment, which is not feasible for the average citizen.
C: Running simulations with chemicals and determining their impact on ecosystems would require specific scientific expertise and access to simulation software, which isn't generally available to the public.
D: Performing 3D scans of proteins requires highly specialized equipment and knowledge, making it unsuitable for citizen science.

Correct Answer
A

A citizen science project is most likely to be successful if it's accessible to the general public and allows for widespread participation. Collecting pictures of birds from around the world (A) is something that many people can do easily, as it doesn't require specialized knowledge or equipment, just a camera or smartphone. This makes it perfect for citizen science, where volunteers contribute data for scientific research.

# Quiz

### Question 1

Each student at a school has a unique student ID number. A teacher has the following spreadsheets available.

- Spreadsheet I contains information on all students at the school. For each entry in this spreadsheet, the student name, the student ID, and the student’s grade point average are included.
- Spreadsheet II contains information on only students who play at least one sport. For each entry in this spreadsheet, the student ID and the names of the sports the student plays are included.
- Spreadsheet III contains information on only students whose grade point average is greater than 3.5. For each entry in this spreadsheet, the student name and the student ID are included.
- Spreadsheet IV contains information on only students who play more than one sport. For each entry in this spreadsheet, the student name and the student ID are included.

The teacher wants to determine whether students who play a sport are more or less likely to have higher grade point averages than students who do not play any sports. Which of the following pairs of spreadsheets can be combined and analyzed to determine the desired information?

- [✔️] A. Spreadsheets I and II
- [ ] B. Spreadsheets I and IV
- [ ] C. Spreadsheets II and III
- [ ] D. Spreadsheets III and IV

### Question 2

A certain computer has two identical processors that are able to run in parallel. The following table indicates the amount of time it takes to execute each of four processes on a single processor. Assume that none of the processes is dependent on any of the other processes.

| Process | Execution Time on Either Processor |
|---------|-----------------------------------|
| P       | 30 seconds                        |
| Q       | 10 seconds                        |
| R       | 20 seconds                        |
| S       | 15 seconds                        |

Which of the following parallel computing solutions would minimize the amount of time it takes to execute all four processes?

- [✔️] A. Running processes P and Q on one processor and processes R and S on the other processor
- [ ] B. Running processes P and R on one processor and processes Q and S on the other processor
- [ ] C. Running processes P and S on one processor and processes Q and R on the other processor
- [ ] D. Running process P on one processor and processes Q, R, and S on the other processor


### Question 3

RunRoutr is a fitness tracking application for smartphones that creates suggested running routes so that users can run with each other. Upon downloading the application, each user creates a username, a personal profile, and a contact list of friends who also use the application. The application uses the smartphone’s GPS unit to track a user’s location, running speed, and distance traveled. Users can use the application to review information and statistics about their previous runs.

At the beginning of a run, users indicate the distance they want to run from their current location, and the application suggests a running route. Once a user accepts a suggested route, the application shares the suggested route with other compatible users in the area so that they can run together. Users are considered compatible if they are on each other’s contact lists or if they typically run at similar speeds.

A basic RunRoutr account is free, but it displays advertisements that are targeted to individual users based on data collected by the application. For example, if a user’s running route begins or ends near a particular store, the application may display an advertisement for that store. Users have the ability to pay a monthly fee for a premium account, which removes advertisements from the application.

- [ ] A. Available running routes near the user’s home
- [ ] B. The current time
- [ ] C. The starting location of the user’s previous run
- [✔️] D. The user’s geographic position

### Question 4

RunRoutr is a fitness tracking application for smartphones that creates suggested running routes so that users can run with each other. Upon downloading the application, each user creates a username, a personal profile, and a contact list of friends who also use the application. The application uses the smartphone’s GPS unit to track a user’s location, running speed, and distance traveled. Users can use the application to review information and statistics about their previous runs.

- [ ] A. Adrianna’s average running speed
- [ ] B. Adrianna’s preferred running distance
- [✔️] C. The current locations of other RunRoutr users
- [ ] D. The usernames on Adrianna’s contact list

### Question 5

RunRoutr is a fitness tracking application for smartphones that creates suggested running routes so that users can run with each other. Upon downloading the application, each user creates a username, a personal profile, and a contact list of friends who also use the application. The application uses the smartphone’s GPS unit to track a user’s location, running speed, and distance traveled. Users can use the application to review information and statistics about their previous runs.

- [ ] A. The application allows users to identify all other users in a particular area.
- [ ] B. Users of the application may be able to easily identify all other users in a particular area as a result of the application's algorithm for determining whether users are compatible.
- [✔️] C. Users of the application may see health benefits as a result of the application encouraging them to exercise with each other.
- [ ] D. Users of the application who live in rural areas have the ability to use all the features of the application, even when they do not have Internet and geolocation connectivity.

### Question 6

RunRoutr is a fitness tracking application for smartphones that creates suggested running routes so that users can run with each other. Upon downloading the application, each user creates a username, a personal profile, and a contact list of friends who also use the application. The application uses the smartphone’s GPS unit to track a user’s location, running speed, and distance traveled. Users can use the application to review information and statistics about their previous runs.

- [ ] A. Users of the application are required to carry their smartphones with them while running in order to enable all of the application’s features.
- [✔️] B. Users of the application may have the ability to determine information about the locations of users that are not on their contact lists.
- [ ] C. Users of the application may not be able to accurately track their running history if they share their smartphone with another family member.
- [ ] D. Users of the application may not be compatible with any other users in their area.


### Question 7

RunRoutr is a fitness tracking application for smartphones that creates suggested running routes so that users can run with each other. Upon downloading the application, each user creates a username, a personal profile, and a contact list of friends who also use the application. The application uses the smartphone’s GPS unit to track a user’s location, running speed, and distance traveled. Users can use the application to review information and statistics about their previous runs.

- [ ] A. Individuals who appear on each other’s contact lists
- [ ] B. Individuals who are interested in running and fitness
- [✔️] C. Individuals who sign up for a premium account
- [ ] D. Individuals whose running routes begin or end near a particular business location

### Question 8

The following table shows the value of an expression based on the values of input1 and input2.

| Value of input1 | Value of input2 | Value of expression |
|-----------------|-----------------|---------------------|
| true            | true            | false               |
| true            | false           | true                |
| false           | true            | true                |
| false           | false           | true                |

Which of the following expressions are equivalent to the value of expression as shown in the table?

Select two answers.

- [✔️] A. (NOT input1) OR (NOT input2)
- [ ] B. (NOT input1) AND (NOT input2)
- [ ] C. NOT (input1 OR input2)
- [✔️] D. NOT (input1 AND input2)
