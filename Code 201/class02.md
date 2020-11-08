# HTML Text

*White space is ignored when rendered but used to make code easier to read.*
1. `<h1-h6>` Six levels of headings starting with h1 as the largest and h6 as the smallest
2. `<p>` Used to designate a paragraph, must have a closing tag `</p>`
3. `<b>` Can be used inline to make text apear bold `</b>`
4. `<sup> & <sub>` Used to create **super script & subscript** text. `</sup> & </sub>`
5. `<br />` Used as a line break, brings text down to a new line
6. `<hr />` Used as a horizontal rule, used between section. Creates a line.
7. `<strong>` Indicates content is important, formats text to bold `</strong>`
8. `<em>` Indicates an emphasis on content, formats text to italic`</em>`
9. `<blockquote>` Is used for a long quote that is paragraph size, effect is an indention of text block `</blockquote>` Should not be used soley for indenting. Use CSS for indent.
10. `<q>` Used for quoting shorter text, puts quotation marks around text. **not recognized by Internet explorer** (Avoid)`</q>`
11. `<abbr title="full-term"> abbr-term</abbr>` Used to identify an acronym or abbreviation
12. `<cite>` Used to reference a piece of work`</cite>`
13. `<dfn>` Used to initally a new terminology within the document`</dfn>`
14. `<address>` Used to contain contact info such as an address, phone number or email `</address>`
15. `<ins>` Used to show text that has  been added (formats text with an underline`</ins>`
16. `<del>`Used to show text that has been deleted (formats text with a strikethrough`</del>`
17. `<s>` Used to idicate content that is no longer accurate but should not be removed `<s>`


# Intro to CSS
*imagine that there is an invisible box around each element*

- CSS works by associating rules with HTML elements
- CSS rules have 2 parts: **Selector** and **Declaration**.
    **Selector** {
        **Declaration**
    }
- CSS **Declarations** have 2 parts: **Property** and **Value**
    Selector {
        **Property: Value**
    }

1. Internal & External CSS
    - Use `<link href="css/styles.css" type="text/css" rel="stylesheet"/>` to link to an external CSS stylesheet.css
    - Use `<Script>`For internal CSS`</Script>`

2. CSS Selectors
    - `* {} - (Universal selector) targets all elements in doc
    - element name {} - (Type selector) targets specific elements
    - .class name {} (Class selector) targets only elements with specific class
    - `# {} - (ID selector) targets elements with specific id
3. CSS rule priority
    - Always applies last rule read
    - More specific rules such as internal or inline can override last rule
    - Typing: **! important** after a rule will take ultimate priority


#Basic Java Script

- Scripting Language (adds behavior)
- JS can be used inline or on a seperate file
- JS runs where it is found in the HTML
- JS is case sensative

# Methods & objects

document.write('good afternoon!')
- object - document
- member operator - .
- method - write('good afternoon!')
- parameters - 'good afternoon!'

1. Statements
- statements are the individual steps in a Script
- they always start on a new line
- they always end with a semicolon ;
- the semicolon indicates that the step is over
- several statements can exist within a code block

2. Comments
- used to keep internal notes on what the code is doing
- for multi line comments use /* xxxxxx */
- for single line commenmts us //
- you can use it to block specific lines of code for testing purposes

3. Variable
- value to store temporary information
- can be reassigned at anytime
- there is no limit to the number of variables or changes
**var quantity; quantity = 3;**
- var - keyword
- quantity - name
- = - operator
- 3 - value

4. Data Types
- numbers (numeric) 
- '"words/letters" (string)'
- true/false values (boolean)

# Decisions & Loops

1. Comparison Operators
- == - is equal to
- != - is not equal to
- === - strick equal to
- !== - strick not equal to
- `> - greater than
- < - less than
- `>= - greater than or equal to
- <= - less than or equal to

2. Logic Operators
- && - logical and
- || - logical or
- ! - logical not

3. If statements
- if (condition) {
    code to execute if true();
}
- If statements evaluate or check if a condition is true. If so the code is executed.

4. If Else staatements
- if (condition) {
    code to execute if true();
}
else {
    code to execute if false();
}
- If Else statements check the condition then execute one code if false or the other if true.