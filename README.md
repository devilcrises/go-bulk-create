# Golang microservices assignment

Read the instructions carefully.
Your ability to understand and follow instructions is part of the evaluation.

Your project will be evaluate from various angles: structure, design, API signature, testing, documentation. Importance should be given to the structure of the project and design of the packages. The correctness of algorithms comes second in relation to API design and idiomatic golang. Your code needs to be easy to follow and to maintain for another developer. I advise you to focus your time in writing the your best code, not in writing a lot of code. It doesn't matter is the service is not complete, we will be able to evaluate what matters to 90poe from a few packages interacting with each other.

## Time limits

The evaluation result of the test is not linked to how much time you spend on it.
Please DO NOT spend more than 2 hours doing it, if you haven't complete the task simply submit as is.
Successful applications show us that 2 hours are more than enough to cover all the evaluation points below. Prefer writing correct code to lots of code.

This assignment is meant to evaluate the golang proficiency of full-time engineers.
Your code structure should follow microservices best practices and our evaluation will focus primarily on your ability to follow good design principles and less on correctness and completeness of algorithms. During the face to face interview you will have the opportunity to explain your design choices and provide justifications for the parts that you omitted.


## Evaluation points in order of importance

- use of clean code, which is self documenting
- use of packages to achieve separation of concerns
- use of domain driven design
- use of golang idiomatic principles
- use of docker
- tests for business logic
- use of code quality checks such as linters and build tools
- use of git with appropriate commit messages
- documentation: README and inline code comments
- you MUST use go modules and a version of go >= 1.15

Results: please share a git repository with us containing your implementation.

Level of experience targeted: EXPERT

Avoid using frameworks such as go-kit and go-micro since one of the purposes of the assignment is to evaluate the candidate ability of structuring the solution in their own way.
If you have questions about the test, please draw your own conclusions.

Good luck.

Time limitations: there are no hard time limits. Once again, do not spend more than ~2 hours.

## Technical test

- Given a file with ports data (ports.json), write a PortDomainService service that either creates a new record in a database, or updates the existing one
- The file is of unknown size, it can contain several millions of records
- The service has limited resources available (e.g. 200MB ram)
- The end result should be a database containing the ports, representing the latest version found in the JSON. Database can be Map in memory
- A Dockerfile should be used to contain the service
- Provide at least one example per test type that you think are needed for your assignment. This will allow the reviewer to evaluate your critical thinking as well as your knowledge about testing
- Your readme.md should explain how to run your program and test it
- The service should handle certain signals correctly (e.g. a TERM or KILL signal should result in a graceful shutdown).

Choose the approach that you think is best (i.e. most flexible).

## Bonus points

- Database in docker container
- Docker-compose file

## Note

As mentioned earlier, the services have limited resources available, and the JSON file can be several hundred megabytes (if not gigabytes) in size.
This means that you will not able to read the entire file at once.
