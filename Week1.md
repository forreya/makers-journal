# Week 1

### Weekly Aims:
1. Learn the basics of test driven development (Rspec) **✓**
2. Gain experience building programs as a pair (driver-navigator, VS live share, git collaborator, git branching) **✓**
3. Understanding the common practices to debugging programs that contain errors. **✓**
4. Gain the skills to be able to design programs to solve problems (single method, single class, maybe multiple class systems(?)) **✓**
---
### Weekly Objectives:
1. Work through the 'Testing Bytes' section (TTD). 
2. Individually debug 3 programs from the 'Skills Challenges'.
3. Begin making a document outlying reasons why test-driving, object-oriented design, debugging, and pairing are powerful practices for software engineers.
4. Everyday, spend the afternoon pairing with another person to work through the 'Golden Square' challenges (implementing practices such as driver-navigator pairing, pushing to/pulling from repositories, utilizing the 'Live Share' extension on VS Code)
5. Watch demonstration videos (after completing the exercises) to pick up new, unthought-of techniques to solving the problem.
---
### Evidence

#### 1. Test Driven Development
- **Test-drove a method** called 'count_words' that takes a string as an argument and returns the number of words in that string, used RSpec to test drive.
- **Test-drove a a single-class program** called 'GrammarStats', used RSpec to test drive.
- **Test-drove a a multiple class-system** with 2 classes, 'Diary' & 'DiaryEntry'.
- **Test-drove a a multiple class-system** with 2 classes, 'TodoList' & 'Todo'.

[Link to repo](https://github.com/forreya/golden-square/tree/main/phase-two)

**Steps to TTD:**
1. Write a small example of how the code might be used in the form of a 'test'.
2. Run the test and see that it fails with an error.
3. Write just enough of the program so that it can passes the test.
4. Improve the readability, structure, and other qualities of the code without changing its behaviour (aka refactoring).
5. Write another small example test, and continue in a cycle until the program can pass a full set of tests that cover every specification.

#### 2. Pair Programming
- Learned the basic syntax of RSpec with @Perspicacity11 by writing simple tests together for straightforward 'single-method' programs. The aim here was to familiarize ourselves with RSpec and the idea of writing preliminary specs for programs that had not been developed yet.
- Pair programmed as a pair for 4 hours with @moeid9 as a Git collaborator [here](https://github.com/moeid9/wk1). Worked on TTD together using VS live share and using Git collaboration.
- Designed multiple multi-class programs [here](https://github.com/forreya/golden-square/tree/main/phase-two) over the course of 2 days. Worked side-by-side with @SimpleLuke in person, debugging our programs and refactoring our code together. Some useful Ruby methods such as 'scan()' and 'reduce()' were learned, along with some complex regex that were used to detect phone numbers from a page of contents.

#### 3. Debugging Programs
- Used 'print' and 'puts' statements to 'gain visibility' of values within my programs (discovery debugging). Debugged [this program](https://github.com/forreya/golden-square/blob/main/phase-two/lib/get_most_common_letter.rb) that initially had errors.
- Used another debugging technique, **binding.irb**, which is an interactive debugger to debug [this program](https://github.com/forreya/golden-square/blob/main/phase-two/lib/letter_counter.rb).

#### 4. Designing Programs
- Created [design recipes](https://github.com/forreya/golden-square/tree/main/phase-two/recipes) for program's interfaces based off user stories. After this, TTD is implemented to develop the specified programs. These completed programs can be found [here](https://github.com/forreya/golden-square/tree/main/phase-two/lib) and the tests / specs can be found [here](https://github.com/forreya/golden-square/tree/main/phase-two/spec).
- Designed a [multi-class journal program](https://github.com/forreya/golden-square/tree/main/phase-two/designing-multi-class-programs) based off a user story (done w/ pair programming). We made a [diagram](https://github.com/forreya/golden-square/blob/main/phase-two/designing-multi-class-programs/recipes/journal.md) to visualize the relationships between classes, created using [asciiflow](asciiflow.com). For the testing, we used a mixture of integration tests & unit tests to test drive the program (RSpec).
- [Video of me](https://github.com/forreya/makers-portfolio/blob/main/videos/task_tracker.mp4) individually test driving a single-method program.
- [Video of me](https://github.com/forreya/makers-portfolio/blob/main/videos/music_tracker-challenge.mp4) individually test driving a single-class program.

**Steps to Designing Multi-Class Programs:**
1. Describe the problem.
2. Design the class system.
3. Create examples as integration tests.
4. Create examples as unit tests.
5. Implement the behaviour.
6. Repeat steps 3-5 until program satisfies all requirements. May also need to revise the design, for example if a mistake was made earlier in the development.
---
### Daily Journal/Notes

#### Day 1:
1. Set up multiple different projects using RSpec, Bundler, Ruby & Git to familiarize myself with setting up an RSpec project for TTD.
2. Pair programmed with @Perspicacity11.

#### Day 2:
Some thoughts: Watching demonstration videos after completing challenges myself helps build onto my existing knowledge and might help me pick up on new programming methods I hadn't thought of before.

#### Day 3:
More thoughts: A weak point of mine is debugging as I tend to just scour through my code until I find the issue, so I must develop good habits and practice 'discovery debugging' as in the long run it'll improve my workflow.
Day summary: Took a day to work from home by myself, worked through some TTD challenges and refined my knowledge on 'discovery debugging'.

#### Day 4:
*Useful Ruby methods that were discovered today:*
1. reduce() - can be used to take an array and reduce it to a single value. For example, can be used to sum all elements in an array with a single line.

Example:
```ruby
def sum(array)
  array.reduce(0) { |sum, num| sum + num }
end
p sum([5, 10, 20])
# => 35
```
2. scan(pattern) - searches through str, matching the pattern (which may be a Regexp or a String). For each match, a result is generated and either added to the result array or passed to the block. I used this method to search for british phone numbers through an array of journal entries by checking if each sub-string in each entry matched the regex given to the scan method.

Example:
```ruby
a = "cruel world"
a.scan(/\w+/)        #=> ["cruel", "world"]
a.scan(/.../)        #=> ["cru", "el ", "wor"]
a.scan(/(...)/)      #=> [["cru"], ["el "], ["wor"]]
a.scan(/(..)(..)/)   #=> [["cr", "ue"], ["l ", "wo"]]
```
---
### End-of-Week Evaluation
*Were all the weekly aims achieved?*
Yes, but some of them were slightly altered/modified towards the end of the week as I became more familiar with the concepts I had aimed to learn. Overall, I am happy with the progress I have made and hope to build upon these skills in the coming weeks.

*Were there any roadblocks/difficulties you had to face?*
The biggest challenge was learning to work with other people for extended periods of time. I have always been a 'lone-wolf' type of individual who would rather do everything alone given the opportunity, and towards the start of the week I was always exhausted by the 2nd hour of pair programming. Collaborating with others will inevitably be mentally draining but I recognize the importance of working with others in industry and so it's important to keep improving upon this skill.