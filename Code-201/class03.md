# Lists

1. Ordered lists **`<ol>`**
- Each list item is placed between a `<li> & </li>` tag
- List is indented automatically by browser
- It will number the list automatically

1. Unordered lists **`<ul>`**
- Each list item is placed between a `<li> & </li>` tag
- List is indented automatically by browser
- Automatically formats list to bullets

1. Definition lists **`<dl>`**
-  Usually contains **terms** & **definitions**
- Will usually find `<dt> & <dd>` elements inside
- `<dt>` will contain the term
- `<dd>` will contain the definition
- Each `<dl>,<dt>, &<dd>` item is placed between a `<li> & </li>` tag

1. Nested lists 
- You can add susequent lists `<ol> or <ul>` inside of one another. (Children)
- All rules from lists still apply

# Boxes

1. Dimensions
- Smallest size to contain content is default
- Define sizes by: 
    - Pixels(px) - Most accurate and most popular*
    - Percentages(xx%) - Relative to window size or containing box 
    - (ems) - Based on the size of text inside (popular for device versatility)

1. Width & Height
- Min & Max define the smallest and largest width a box can have
- Min & Max height works the same as width
- To maintain aspect ratio it is reccomended to only use one or the other

1. Overflowing content
- Tells the browser what to do with content that does not fit
- Hidden Property
    - Used to designate content to be hidden when all cannot fit
- Scroll property
    - Used to add a scroll bar to content that is not visible

1. Centering content
- Set *left-margin* & *right-margin* to **auto** to center inside current element
- The *text-align* property **IS** inherited by child elements

1. Change Inline/Box elements
- Allows you to convert an inline element to a box element  or vice versa
    - **inline** - Causes block elements to behave like an inline element
    - **block** - Causes an inline element to behave like a block element
    - **inline-block** - Casues a block element to flow like an inline element with block features
    - **none** - Completly hide the element from the page but is still visible in source code

1. Shadows
- Allows you to add a drop shadow around box (similar to **text-shadow**)
    - Horizontal offset - 0 is cented, negative values moves shadow left
    - Vertical offset - 0 is center, negative values moves shadow left
    - Blur distance - If omitted shadow is a solid line (border) 
    - Spread of shadow - 0 is center, negative values moves shadow closer positive moves shadow out in all directions


1. Hiding boxes
- Hides boxes from page but leaves a blank space
- **hidden** - Hides the element
- **visible** - Shows the element

# Border, Margin, & Padding
- Every box has these 3 properties that can be modified

1. Border
1. **border-image** - Applies an image to border of any box
- Property requires 3 inputs
    1. Source/URL of image
    1. Where to slice image
    1. What to do with edges
- Possible values are **stretch, repeat, round**
- Box must have a border width assigned

1. Margin
- Specifies the gap between boxes
- If one box sits on top of another they are **Collapsed**
- Width is automatically calculated for height and vice versa
- You can adjust **Top, Right, Bottom, & Left** individually or together (Clockwise)
- this property is not inherited by child elemets

1. Padding
- Specifies the space between content and border
- You can adjust **Top, Right, Bottom, & Left** individually or together (Clockwise)
- This property is not inherited by child elements

1. Rounded corners
- **border**-xxx-xxx-**radius** insert top, bottom, left, right
- Used to specify each corner
- Kepp values the same for uniformity or different to make a custom shape
- Usually defined in **px**

# Switch Statements
- Starts with a **switch** value
- Each subsequent case tests a specific set of possible values
- Only runs the positive match (**If Else** runs each possible value *slower*)
- Data tyoes can be changed because of **type coercion**

1. Truthy & Falsy
- Due to type coercion evry value in JS can be treated as true or false
- A value 0 or "null" cal give a *falsy* value
-  Truthy values can be treated as 1
- The presenvce of an object or an array canalso produce a *truthy* value

1. Equality &  Exsistance
- A **Unary** operator returns a result with just one operand
- Use **=== & !==** instead of **== & !==** for  les unexpected values

1. Short circuit values
- Logical operator operate left to right
- They short-circuit or **Stop** as soon as they have a result
- They return the value that caused the *stop*

# Loops

1. Loop counters

- Keywords
    - break - Causes a termination of the loop
    - continue - Tells the interpreter to continue with the current iteration
- Loops check a condition
- A loop will continue to run the code while condition is true
- It will terminate upon a false result of the condition

1. Loop Counters
- **var i = 0** - *Initialization* - Create a variable(i) *Acts as the **Counter***
- **i = <10;** - *Condition* - The loop will continue to run until it reaches specified number
- **i++** - *Update* - Everytime it runs the ++ will add 1 to the variable

1. For Loops
- Often used to loop through an array
- Total number of items is stored  in a variable called **arrayLength**
- **roundNumber** holds the round of the test
- **test;msg** holds the message to display
- **i** is the counter displayed outside the loop
- Written as **`for (var i = 0; i < 10; i++) {Code to execute during loop}`**

1. While Loops
- Runs while the condition is true
- Write a message for each time it is run

1. Do While Loops
- Main difference between while loop is the the statement comes before the condition


