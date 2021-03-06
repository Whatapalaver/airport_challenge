Airport Challenge - Week 1 Progress
====================================
This the solo weekend challenge from the end of week 1 at Makers.

By the end of week 1 all Makers developers can:

- Test-drive a simple program using objects and methods  
- Pair using the driver-navigator style  
- Follow an effective debugging process  
- Describe some basic OO principles like encapsulation, SRP  

Approach
--------
I initially started this challenge wit a combination of wading in with the code and dabbling in rspec. Now I'm onto Day3 and I have sussed out the whole TDD process of feature testing and unit testing, I realise I should be using this method to help me crack the airport challenge.

This will involve a little bit of back tracking.....


```
        ______
        _\____\___
=  = ==(____M_____)
          \_____\___________________,-~~~~~~~`-.._
          /     o o o o o o o o o o o o o o o o  |\_
          `~-.__       __..----..__                  )
                `---~~\___________/------------`````
                =  ===(_________)

```

User Stories
------------

We have a request from a client to write the software to control the flow of planes at an airport. The planes can land and take off provided that the weather is sunny. Occasionally it may be stormy, in which case no planes can land or take off.  Here are the user stories that we worked out in collaboration with the client:

```
As an air traffic controller 
So I can get passengers to a destination 
I want to instruct a plane to land at an airport 
```

Feature: Plane lands at airport

```
As an air traffic controller 
So I can get passengers on the way to their destination 
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport
```

Feature: Plane to take off and enter airspace

```
As an air traffic controller 
To ensure safety 
I want to prevent takeoff when weather is stormy 
```

Feature: Take off not possible when weather is stormy

```
As an air traffic controller 
To ensure safety 
I want to prevent landing when weather is stormy 
```

Feature: Landing not possible when weather is stormy

```
As an air traffic controller 
To ensure safety 
I want to prevent landing when the airport is full 
```

Feature: Landing not possible when airport full

```
As the system designer
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate
```
Feature: Airport has default capacity which can be overidden

Features to be Tested in RSpec Features:
========================================
- [x] Plane lands at airport  
- [x] Plane to take off and enter airspace  
- [x] Take off not possible when weather is stormy  
- [x] Landing not possible when weather is stormy  
- [x] Landing not possible when airport full  
- [x] Airport has default capacity which can be overidden  


## User Stories Complete - Additional Tasks

- [x] Your task is to test drive the creation of a set of classes/modules to satisfy all the above user stories.  
- [x] You will need to use a random number generator to set the weather (it is normally sunny but on rare occasions it may be stormy).  
- [x] In your tests, you'll need to use a stub to override random weather to ensure consistent test behaviour.  

Your code should defend against [edge cases](http://programmers.stackexchange.com/questions/125587/what-are-the-difference-between-an-edge-case-a-corner-case-a-base-case-and-a-b) such as inconsistent states of the system ensuring that: 
- [x] planes can only take off from airports they are in;  
- [ ] planes that are already flying cannot take off and/or be in an airport;  
- [x] planes that are landed cannot land again and must be in an airport, etc.  

For overriding random weather behaviour, please read the documentation to  
- [x] learn how to use test doubles: https://www.relishapp.com/rspec/rspec-mocks/docs . There’s an example of using a test double to test a die that’s relevant to testing random weather in the test.  

## Code Review
In code review we'll be hoping to see:
* All tests passing
* High [Test coverage](https://github.com/makersacademy/course/blob/master/pills/test_coverage.md) (>95% is good)
* The code is elegant: every class has a clear responsibility, methods are short etc. 
Reviewers will potentially be using this [code review rubric](docs/review.md).  Referring to this rubric in advance will make the challenge somewhat easier.  You should be the judge of how much challenge you want this weekend.

**BONUS**
- [x] Write an RSpec **feature** test that lands and takes off a number of planes

**ISSUES TO RESOLVE**
- [ ] I am stubbing randomness from the airport stormy? method and not the Weather class
- [ ] My tests to see if plane flying etc use an Airport array and so will only include planes that have taken off from the same instance of airport. I need to amend to show a global planes array of flying? landed?

