#### The best applications are coded properly. This sounds like an obvious statement, but by ‘properly’, I mean that the code not only does its job well, but is also easy to add to, maintain and debug.


### 1 - Limit line length(120 max)
Long lines are hard to read. It is a good practice to avoid writing horizontally long lines of code. Limit the line to maximum 120 characters. If the line gets longer than that, divide it into multiple lines.

Limit the comment to 72 characters only.

### 2 - Continuation line over-indented for hanging indent
Although hanging indent is a part of PEP 8 gudilines but we can use it to break code in multiple lines effectively.
##### Anti-pattern
```csharp
 // Arguments on first line forbidden when not using vertical alignment.
 var a  = someObject.LongFunctionName("csharp", "value 1", "value 2"
          OtherFunction(val1, val2))
          
 // Further indentation required as indentation is not distinguishable.
 public void MyFunction(
             value1, value2, 
             Value3,
             value4)
 {
     //..
 }

```
##### Best practice
```csharp
 // Aligned with opening delimiter.
 var a  = someObject.LongFunctionName("csharp", "value 1", "value 2"
                                      OtherFunction(val1, val2))

 // Aligned with opening delimiter.                         
 public void MyFunction(value1, value2, value3,
                        value4)
 {
     //..
 }
 
 // Add a tab spaces (an extra level of indentation) to distinguish arguments from the rest.                              
 public void MyFunction(
                value1, value2, value3,
                value4)
 {
     //..
 }
 
 // Hanging indents should add a level.
 var a  = someObject.LongFunctionName(
              "csharp", "value 1", "value 2"
              OtherFunction(val1, val2))
 
```

##### However, know when to be inconsistent -- sometimes style guide recommendations just aren't applicable. When in doubt, use your best judgment. Look at other examples and decide what looks best. And don't hesitate to ask!
##### Some other good reasons to ignore a particular guideline:</br>
1 - When applying the guideline would make the code less readable, even for someone who is used to reading code that follows this guideline.</br>
2 -To be consistent with surrounding code that also breaks it (maybe for historic reasons) -- although this is also an opportunity to clean up someone else's mess.

### 3 - Separate any logical statement by a new line

```csharp
var myVariable = someObject.MyFunction();

if(condition)
{
    //..
}
```
### 4 - Limit the function to 30 lines
A function must be of 30 lines. If it's exceeding please create seperate helper function.

### 5 - Use 'using' wherever possible
When you are using an object that encapsulates any resource, you have to make sure that when you are done with the object, the object's Dispose method is called. This can be done more easily 'using' the using statement in C#.

### 6 - Use appropriate prefix for each of the UI elements
| Control                   | Notation   |
|:--------------------------|:-----------|
| Label                     | lbl        |
| TextBox                   | txt        |
| DataGrid                  | dtg        |
| Button                    | btn        |
| ImageButton               | imgb       |





