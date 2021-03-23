### Chapter 1

#### Stylesheet Origin
Stylesheets can come from several different origins
- author styles are the ones you add
- user agent styles are the browser's defaults
- user stylesheet sits in the middle priority between author and user-agent (not used very often)

User agent styles are lower priority, and are overriden by author styles. They vary browser to browser, but have the same things generally. For example, headers and p tags have top an bottom margins, lists have left padding, and link colors and default font-sizes are set.

#### Terminology

Declaration: ```color: black;```
Declaration Block:
```
body {
    color: black;
    font-family: helvetica
}
```

Selector: the part that comes before the curly braces
Ruleset: the combination of a selector and the declaration block that accompanies it
At-rules: language constructs beginning with an @ such as @import or @media

#### Cascade rules
After user-agent styles are applied, the browser applies author styles

An exception to style origin rules is the !important rule

#### Specificity
The browser evaluates specificity in two parts: styles applied inline in html and styles applied with a selector

Inline styles (in html) are applied directly to the element and override any declarations.

Selector Specificty rules:
    - If a selector has more IDs it wins
    - If that results in a tie, the selector with the most classes wins
    - If that results in a tie, the selector with the most tag names wins

    Pseudo class selectors and attribute selectors each have the same specificity as a class selector

    Easiest way to remember is to specify with numbers. 
    #id,#classes,#tags
    1,2,2

    Best practice is to keep specificity low where you can

#### Source order
Order in which the Ruleset comes in. Applies if specificity and origin are the same.

For link styles, follow the LoVe/HAte - link, visited, hover, active

cascaded value: The declaration that "wins"

#### Advice
Don't use ID's in your selector
Don't use !important

There are exceptions where they are okay, but they should not be the first thing you reach for

#### Inheritance
Cascade and Inheritance are related, but not the same

Not all properties are inherited, but things related to text often are

##### Using initial
Initial keyword sets the style to a default
Is not supported in IE

#### Shorthand properties
Properties that let you set the values of several other properties at one time

Most shorthands let you omit certain values and only specify what you're concerned with. Doing this still sets the omitted values, (to the initial value)

Avoid using font: as a shorthand as it contains a lot of styles

For shorthands on margin or padding, the properties go clockwise starting from the top

TRouBLe is a mneumonic you can use to remember the order