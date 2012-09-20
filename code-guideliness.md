# C# Coding Guideliness

* Always clear all comments when work is done no matter if is yours or not.

* Always wrap in {} [if, for, foreach,…] statement even the one line code.
  One liner rule is when there is possibilty that code will expand, mostly always!
  Except when there is a single condition and then the line for throwing exception is the when {} can be omited, because this code will never expand in multi-line.

    ```csharp
    // good
    if (isGood) { return good; }

    // bad
    if (isGood) return good;

    // except
    if (isGood) throw new TooGoodTooBeTrueException("Some valid description");
    ```

3. Before the start of [if, for, foreach,…] block and end of block statement make one break space.
4. Always use string.Empty instead of ""
5. Inline comment should be right above the line it is commenting without break space.

    Correct:
    // Set is good to be good. The ok inline comment
    bool isGood = true;

    Incorrect:
    // Set is good to be not. The not ok inline comment

    bool isGood = false;

6. Do not use #Region for hiding the code. Better is to move the code to the end of the class. Or use VS keys [Ctrl+A [Ctrl+M, Ctrl+M]] that will collapse whole document.
7. The order of members in Class should be:
	* Fields.
		* Constants always first. 
	* Constructor(s).
	* Properties (If there are many like in ViewModels it can be moved to the end of Class, but not those that have some logic).
	* Public Methods.
	* Protected Methods.
	* Private Method.	
8. Preferably use "this" keyword for all members within a current Class and those inherited Class(es).
9. All private fields should start with underscore as:
    this._isGood 
10. Use Interfaces for mostly everything, or use Abstract Classes when appropriate.
11. Avoid inheritance from normal Class, inherit from Abstract Class.
11. Avoid deeply nested inheritance, the one level of inheritance should be preferable.
12. Use Dependency Injection / Inversion of Control in all cases and avoid "new" keyword for creating the Object(s).
13. In Interface put a each member with break space in between.
14. Do not write long statements something like more than 100 chars.
15. Break the "if" conditions in multiple lines if there are many of them.
16. Use ternary operator "?:" with caution, better write "if-else" if the statement is logically complex to understand or the statement will be long because of it.
17. Remove any break spaces in code that are more than one line or they are one line but they have no sense to be applied at first place! 
18. User "var" keyword only when on right side there is Type [int, string, Order, List<Order>,…].
Exception: Use "var" for LINQ queries only if the result is of "Anonymous Type".
    Correct:
    var goods = new List<Good>();

    Incorrect:
    var goods = this.GetGoodsById(goodId);  

    Correct:
    ICollection<Good> goods = this.GetGoodsById(goodId);
19. Write logical/meaningful names especially in services or APIs, no matter how long they can be.
20. If the member is of bool return type make sure it is called proper with [is|has|have] at the beginning of sentence. 
21. If there are local variables in method make sure that they are at the beginning of method.
22. If there is need for some Class member repeatedly, make variable of it and use variable instead.
e.g if this expression is used more then one time:
this.teamDropDown.SelectedItem as Team
make variable and use it instead:
var team = this.teamDropDown.SelectedItem as Team;
23. Avoid "static" Fields, Properties in all cases. Use "static" for "Helper" or this kind of Class(es) only. Also for use it for simple Methods if "static" is applicable.
24. On asynchronous call, if there is more than 5 lines of code, use a Callback Method (and give meaningful and callback like name to method) instead of inline Lambda. 


Exception Handling!!
Null Reference checking!!
