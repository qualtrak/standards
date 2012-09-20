# C# Coding Guideliness

* Always clear all comments when work is done no matter if is yours or not.

* Always wrap in `{}` [`if`, `for`, `foreach`,…] statement even the one line code.
  One liner rule is when there is possibilty that code will expand, mostly always!
  Except when there is a single condition and then the line for throwing exception is the when `{}` can be omited, because this code will never expand in multi-line.

    ```csharp
    // good
    if (isGood) { return good; }

    // bad
    if (isGood) return good;

    // except
    if (isGood) throw new TooGoodTooBeTrueException("Some valid description");
    ```

* Before the start of [`if`, `for`, `foreach`,…] block and end of block statement make one break space.

* Always use `string.Empty` instead of `""`

* Inline comment should be right above the line it is commenting without break space.

    ```csharp
    // good
    // Set is good to be good. The ok inline comment
    bool isGood = true;

    // bad
    // Set is good to be not. The not ok inline comment

    bool isGood = false;
    ```

* Do not use #Region for hiding the code. Better is to move the code to the end of the class. Or use VS keys [Ctrl+A [Ctrl+M, Ctrl+M]] that will collapse whole document.

* The order of members in Class should be:
	* Fields.
		* Constants always first. 
	* Constructor(s).
	* Properties (If there are many like in ViewModels it can be moved to the end of Class, but not those that have some logic).
	* Public Methods.
	* Protected Methods.
	* Private Method.	

* Preferably use "`this`" keyword for all members within a current Class and those inherited Class(es).

* All private fields should start with underscore as:

    ```csharp
    private bool _isGood 
    ```
* Use Interfaces for mostly everything, or use Abstract Classes when appropriate.

* Avoid inheritance from normal Class, inherit from Abstract Class.

* Avoid deeply nested inheritance, the one level of inheritance should be preferable.

* Use Dependency Injection / Inversion of Control in all cases and avoid "`new`" keyword for creating the Object(s).

* In Interface put a each member with break space in between.

* Do not write long statements something like more than 100 chars.

* Break the "`if`" conditions in multiple lines if there are many of them.

* Use ternary operator "`?:`" with caution, better write "`if-else`" if the statement is logically complex to understand or the statement will be long because of it.

* Remove any break spaces in code that are more than one line or they are one line but they have no sense to be applied at first place! 

* User "`var`" keyword only when on right side there is Type [`int`, `string`, `Order`, `List<Order>`,…].
Exception: Use "`var`" for LINQ queries only if the result is of "Anonymous Type".

    ```csharp
    // good
    var goods = new List<Good>();

    // bad
    var goods = this.GetGoodsById(goodId);  

    //good
    ICollection<Good> goods = this.GetGoodsById(goodId);
    ```

* Write logical/meaningful names especially in services or APIs, no matter how long they can be.

* If the member is of bool return type make sure it is called proper with [is|has|have] at the beginning of sentence. 

* If there are local variables in method make sure that they are at the beginning of method.

* If there is need for some Class member repeatedly, make variable of it and use variable instead.

    ```csharp
    // e.g if this expression is used more then one time:
    this.teamDropDown.SelectedItem as Team

    // make variable and use it instead:
    var team = this.teamDropDown.SelectedItem as Team;
    ```

* Avoid "static" Fields, Properties in all cases. Use "static" for "Helper" or this kind of Class(es) only. Also for use it for simple Methods if "static" is applicable.

* On asynchronous call, if there is more than 5 lines of code, use a Callback Method (and give meaningful and callback like name to method) instead of inline Lambda. 

Exception Handling!!
Null Reference checking!!
