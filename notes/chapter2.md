#### Chapter 2

Working with relative units

Pixels: absolute units (most commonly known)

Due to the unpredictable nature that is the browser size, styles can't be applied based on an ideal context

##### EMs and REMs

Ems: the most common relative unit length
    - measure used in typography
    - 1em means the font size of the current element
    - Values declared using relative units are evaluated by the browser to an absolute value, called the "computed value"

Font-size ems are declared by the inherited font size
    -ems is not great to use for fonts 

Rems for font-size
    Short for root em
    - Instead of being relative to the current unit, rems are relative to the root element 

    1.2 rem has the same computed value

    For accessibility, the default font size set with pixels does not scale, but with rems it does. You should always specify fonts with rems or percentages

When in doubt: rems for font size, pixels for borders and ems for other properties

##### Viewport Relative Units
ems and rems are defined relative to the font-size, but there are also viewport relative units for defining lengths relative to the viewport

vh - 1/100th of the viewport height
vw - 1/100th of the viewport width
vmin - 1/100th of the smaller dimension
vmax - 1/100th of the larger dimension

##### Using calc() for font-size
calc() lets you do basic arithmetic with two or more values.
support +-*/ and needs whitespace inbetween the operators

##### Unitless numbers and line-height
unitless values: a number with no specified unit
 - line-height
 - z-index
 - font-weight

 line-height property is unusual (accepts both units and unitless values)

 ##### Variables
 Declared with (--) followed by whatever name you want
 Must be declared in a declaration block

 By itself, the declaration does nothing, to use it, call the var() function and give it the variable name

 Var takes a second parameter which is a fallback style 
