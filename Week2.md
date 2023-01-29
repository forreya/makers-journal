# Week 2

### Weekly Aims:
1. Learn to unit test parent-child classes & peer classes. **✓**
2. Learn to craft doubles for specific purposes such as for verifying that a class does its job correctly. **✓**
3. Learn to test API requests using RSpec doubles. **✓**
4. Learn to unit test terminal IO using RSpec doubles. **✓**
---
### Weekly Objectives:
1. Finish the 'Mocking Bites' section (isolating tests using RSpec). 
2. Watch through the example solutions for 'Mocking Bites' to understand the typical procedure used when isolating tests for individual classes by using doubles.
3. Aim to complete the solo project from phase 4 to fully assimilate all the learning from 'Mocking Bites' section.
4. Only if there is time, begin and try to complete the optional 'Battleships' challenge.
---
### Evidence

#### Main Project - Food Ordering System
[Link here](https://github.com/forreya/food-ordering-system). Skills practiced & challenges faced:
1. Designing a program based on user stories. My recipe included a flow chart diagram that was created on _asciiflow.com_, integration tests, unit tests, and lastly the code itself.
2. The program was split into 3 classes, a parent class 'Cart' & 2 child classes, 'Dish' & 'Menu'. This is illustrated in my flow-chart diagram or my preliminary classes-design- both of which can be found in my program [recipe](https://github.com/forreya/food-ordering-system/blob/main/recipe/food-recipe.md).
3. The biggest challenge was creating a double to mock the `twilio-ruby` functionality, but eventually I created a complex double that excactly mimicked `twilio` and my understanding of mocking improved so much. Understanding this idea was crucial in being able to fully test whether the correct delivery texts were being sent. These tests can be found [here](https://github.com/forreya/food-ordering-system/blob/main/spec/integration_spec.rb).  
4. I tried my hardest to follow the concept of test-driven development throughout this project and created the test examples in the [recipe](https://github.com/forreya/food-ordering-system/blob/main/recipe/food-recipe.md) first, followed by actually writing the RSpec integration tests (adding unit tests as required), followed by finally implementing the code needed to pass the tests.

#### 1. Unit Testing Parent-Child Classes & Peer Classes
- **Use mocking techniques to add unit tests** that fully test the behaviour of the class 'TaskList', which is a parent class of 'Task'. Found [here](https://github.com/forreya/mocking-bites).
- **Test-drove 2 peer classes**, 'SecretDiary' & 'Diary', by using integration tests and exercising _all_ of the class's functionality, without using or referring to the other class. Found [here](https://github.com/forreya/golden-square/tree/main/phase-3).
- **Test-drove a class** called 'TaskFormatter using unit tests and mocking. Found [here](https://github.com/forreya/golden-square/blob/main/phase-3/spec/task_formatter_spec.rb).

#### 2. Crafting Doubles
- Learned that doubles are tools used to test that one class interacts with another in the correct way. A double acts the same as the collaborator class, and verifies that the tested class does its job correctly.
- To do this we have to create a double whose public interface matches the public interface of the class we're trying to test.

Throughout this week I incorporated doubles in essentially _all_ my RSpec tests, including:
- **Creating doubles to pass all the tests** in [this](https://github.com/forreya/golden-square/blob/main/phase-3/spec/doubles_exercise_spec.rb) exercise, which involved setting up doubles that take arguments, doubles that expect to be called & doubles created for a _specific_ scenario.
- **Creating doubles to pass all the tests** in [this](https://github.com/forreya/golden-square/blob/main/phase-3/spec/doubles_challenge_spec.rb) challenge, which involved creating sophisticated doubles.

#### 3. Testing API Requests Using Doubles
- **Unit tested an API-dependent class called TimeError**,that returns the difference in seconds between the server time and the local computer time. This involved creating a double for Net:HTTP and also dealing with the behaviour of Time.now which is non-deterministic. Found [here](https://github.com/forreya/golden-square/blob/main/phase-3/spec/time_error_spec.rb).
- **Unit tested an API-dependent class called 'CatFacts'** which retrieves random cat facts from an API and returns it. Found [here](https://github.com/forreya/golden-square/blob/main/phase-3/spec/cat_facts_spec.rb).

#### 4. Unit Testing Terminal IO using RSpec doubles
- **Test drove a class** that asks the user for 2 numbers and subtracts them from each other. Intrinsically, this is a simple program to develop. However, the point of this exercise was to create doubles for puts and gets so I could check and control them. This was done using the special object, _Kernel_, and creating a double for it. This RSpec tests can be found [here](https://github.com/forreya/golden-square/blob/main/phase-3/spec/interactive_calculator_spec.rb).
- **Test drove a class** that asks the user for a string and an integer, then repeats that string the same number of times as the integer. This RSpec tests can be found [here](https://github.com/forreya/golden-square/blob/main/phase-3/spec/string_repeater_spec.rb).
---
### Daily Journal/Notes

#### Day 1:
Had trouble understanding the concept of mocking ( creating fake classes, _doubles_, for testing purposes). The specs for each unit test and the main integration test file were starting to clutter and was getting quite confusing as they had very similar names & tested similar methods. Had to watch the demonstration video fully to really understand the standard procedure when implementing 'mocking'.

#### Day 3:
Finished up all of the 'Mocking Bites' section and the idea of _doubles_ for unit testing now makes a lot more sense. Now beginning on the solo project to consolidate my all my learning for the first 2 weeks of Makers. This project will be designed and developed from scratch based on some user stories.

#### Day 5:
Finished my [food-ordering system](https://github.com/forreya/food-ordering-system) which implements `twilio-ruby` to send texts to the user's phone number, informing them of the expected delivery time (calculated based on current server time, retrieved from an API) after an order is placed. This program allows the user to see a menu with prices, select from the available dishes, and see an itemised receipt with a grand total price.
---
### End-of-Week Evaluation
*Were all the weekly aims achieved?*

All the aims were not only learned, but fully absorbed and ingrained in the way I write code now. This was especially reinforced by the `food-ordering` project I undertook. Although I didn't get to begin on the `battleships` project, I believe that my learning this week has prepared me with more than enough of a solid foundation for next week; where I'll be learning about SQL.

*Were there any roadblocks/difficulties you had to face?*

The concept of mocking seemed at first quite redundant and unnecessary but as I became more familiar with _how & why_ doubles are used in testing, it eventually became clear how important testing **all** of a class's functionalities was. For me, implementing doubles- especially with more complicated objects like APIs & the terminal- was definitely the biggest challenge this week (more so the conceptual side of it rather than the coding aspect).