Project 3 Submission Guidelines
===============================

#### There will be no extra credit or early grading opportunities for Project 3. See below for details regarding the functionality check opportunity.

#### There will be no interactive grading for Project 3. Instead, grading will occurs as follows:
1. After the deadline the instructor will execute a client program that will perform one or more tests for each of the Functionality Criterion described in the [Project 3 assignment specification](https://github.com/CS601-F18/projects/blob/master/project3.md). 
  - If a student's solution is not deployed and running on the microcloud VM node specified in the assignment _when the tests are executed_ that student will earn a score of 0 for all Functionality Criterion. The tests may be executed anytime after the deadline and it is expected that a student's continue to run and function correctly until the instructor indicates it is safe to stop the process. A solution that is not deployed correctly will not be eligible for Design resubmission for this project.
  - If a student's solution is deployed and running but does not correctly implement the APIs required the student will earn only partial credit for all Functionality Criterion.  In this case, the student will not be eligible for Design resubmission for this project.
2. An instructor or TA will review all code, including the Part 4 test code, and assign a Design grade. Students who pass all Functionality tests and have not already completed two project resubmissions will be eligible for resubmission of Project 3.


#### Each student may come in for *one* early functionality check.
1. The early functionality check must be completed with the instructor.
2. During the meeting, the instructor will execute a program that will run all functionality test cases against the student's solution deployed on the assigned microcloud VM. 
  - Test cases will **not** be run against a locally deployed solution, for instance on a student's laptop. The solution must be running on the student's [primary VM node](https://github.com/CS601-F18/notes/blob/master/admin/mcassignments.md) on the correct port.
  - The test program will not be provided to the student.
3. The result will be PASS or FAIL only. The instructor will not provide additional detail regarding why a student's solution did not pass the test cases. It is up to the student to debug his/her solution if the functionality check does not pass. 
4. **If a student returns for an additional functionality check FIVE (5) points will be deducted from the student's final project score for each return visit.** It is expected that a student has thoroughly tested his/her solution before coming for the functionality check. *The functionality check is not an opportunity for the student to use the instructor to test his/her code.* If the student's solution is not deployed correctly, or if it fails any of the test cases, he/she will not be eligible for a second functionality check without the aforementioned deduction being applied.
5. The functionality check does not include a code review. 
6. Functionality check appointments may be scheduled on the [functionality check appointment calendar](https://calendar.google.com/calendar/selfsched?sstoken=UUFES3ZubHpYZXF3fGRlZmF1bHR8YTBiYWJjZjM3MTdjY2Q5ZjZhOTQ3ZDVlZDI1MmJhNjg). Appointments are THREE (3) minutes long. Do not sign up unless you are certain your solution will be complete, well tested, and deployed to your primary microcloud VM node by the appointment time.

#### Other Advice 
1. You may limit the size of the `InvertedIndex` used in Part 2 to 10,000 records.
2. It is strongly recommended that you implement thorough logging in your solution. This will help you debug if you come for the functionality check and fail. Your logs should indicate which requests were made to your server and where your server went wrong.
3. Consider using curl or another client program to test your deployed solution. Below are a few requests to get you started.

```
# correct GET /reviewsearch
curl -v "http://<host>:<port>/reviewsearch"

# correct POST /reviewsearch
curl -v -X POST --data-urlencode "query=computer science" "http://<host>:<port>/reviewsearch"

# incorrect POST /reviewsearch
curl -v -X POST --data-urlencode "BADquery=computer science" "http://<host>:<port>/reviewsearch"
```
