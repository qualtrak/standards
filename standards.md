# Code Standards

* Keep code clean of all commented code, especially if is a left-over.
* Avoid deeply nested inheritance, one level of inheritance (parent/child) is preferable.
* Make sure that in inheritance, the parent class is abstract and have in name Base or Abstract to denote it.
* Avoid inheritance from non abstract class.
* Avoid long code lines when there is logic inside, break it in to local variables.
* Break if statements in new line when there are multiple conditions inside.
* Break line on conditionals (&&, ||, !) when breaking if statement.
* Avoid commenting code inline, better write test with meaningful test name.
* Avoid writing documentation comments except if comments are generated (e.g. for API) and read often so it is up to date.
* For other not public parts of code rather write tests than documentation, that will most certainly not be up to date.
* Try to give meaningful names to classes, methods and variables no matter how long it will be.
* Especially give meaningful names for all publicly available interfaces (e.g. REST API).
* Stick to Law Of Demeter by avoiding chaining of more than two classes (e.g. tenant.unit.team.name Tenant shouldn't interact with Team only Unit).
* Try to stick to Single Responsibility Principle for classes and methods too.
* Try to write methods below 10 LOC and avoid write methods longer than 40 LOC especially if it contains lots of conditional statements, better refactor it to more properly named methods.
* Try to write classes below 100 LOC.
* Refactor code often when there is a space for improvement.
* Stick to Don't Repeat Yourself and minimize the duplication of code and refactor it afterwards.
* Write code that can expand and is loose coupled.
* Test Driven Development should be goal, writing incrementally and only enough to satisfy the test.
* Behavior Driven Development for testing a set of functionalities or whole feature.
* Coding discipline, consistency and testing should	be main motto.
* Build project before checking source to repository.
* After finishing task or feature or big piece of functionality clean up code from unnecessary comments, apply check-in best practices, spaces, rename poorly named methods/variables build project and commit the code.
* Write meaningful commit message before commit.
* If the Revision Control is Distributed then make sure to pull latest version before pushing to repository to avoid merging.
* Features and Source Control: Branch per Feature or not???
* Acceptance testing with scenarios provided by QA.
* Make sure to learn different languages and coding techniques.
* Use, learn and experiment Design Patters wherever/whenever is applicable.
