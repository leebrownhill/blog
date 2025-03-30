+++
date = '2025-03-23T17:19:39Z'
draft = true
title = 'SQL Unit Testing Using tSQLt: Part 1'
featured = 'img/featured/tsqlt_logo.png'
+++

<br>

### Unit...what now?

Other practitioners of code slinging, such as .net folks, have been unit testing their code for many moons now. Us SQL folks however rarely seem to do this from what I have seen.
A few job roles ago now, I had to use unit testing on a daily basis. It was heavily integrated into our work flow via the CI/CD pipelines we used. Ultimately, if you checked some code in, you made sure you had the associated unit tests written for it.
As with many things of this nature, initially, it felt like a chore; an unnecessary extra that needed thinking about all of sudden.
One day however, a unit test caught an error in one of my procedures (dear reader, I was as shocked as you probably are). The unit test caught an edge case bug in my code, one which would never have found with basic smoke testing. 
From that day, I have been a passionate advocate for unit testing.

Better egg on ones face, than omelettes in production

<br>

### Unit Testing Defined

While it may seem obvious to some, a loose definition of 'unit testing' would be:
>*Testing the smallest part (unit) of one’s application code. Providing some standard inputs and preempting its >output(s) to validate the unit’s functionality*

[GeeksforGeeks](https://www.geeksforgeeks.org) have a comprehensive guide [here](https://www.geeksforgeeks.org/unit-testing-software-testing/#what-is-unit-testing) regarding what unit testing is actually comprised of.

<br>

### So what is tSQLt?

[tSQLt](https://tsqlt.org/) is an open-source framework used for the purposes of unit testing SQL Server code. APIs are also available making it possible to integrate nicely into CI (Continuous Integration) services such as TFS and Azure DevOps.
Some key features and benefits:
- Write tests in T-SQL – an obvious benefit. No need to learn additional or external tools
- Tests are all run within transactions keeping your test independent (and idempotent) thus minimizing clean up work
- Create unit tests directly by Schema – create dedicated tests for specific areas of your product/code base and run those independently
- Provides the functionality of being able to ‘mock’ tables and stored procedures allowing for easier testing of code functionality
- Totally free to use
- Completely customizable

<br>

### Great! But how can it help me?

The main benefit tSQLt has given me is assurance in stored procedure changes I have made. 
Its enabled me to have confidence that the core functionality of a procedure has remained the same after i have made changes to it.
The ability to totally isolate the stored procedure's functionality and verify it, has been a huge support for me over the years. Paired with the great Redgate tool [SQL Test](https://www.red-gate.com/products/sql-test/), its the ultimate comfort blanket for code noodlers™.

<br>

### Looking Forward

I am once again working in an environment where I know tSQLt is going to help me. I currently have several projects on the go where I can see the need for unit testing.
So with that said, i'm dusting off the cobwebs of my tSQLt install to get to know my old friend again. I do hope you come along for the journey.

In the next post, we shall go through a full demo using the bare mechanics of the framework. 
I plan to publish a few posts regarding tSQLt covering a number of its functions and features as we go.


Thanks for reading!