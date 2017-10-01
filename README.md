

# Regex

. used to match any character execpt newline

^ used to indicate start of the line

$ used to indicate end of the line

[abc] used to match character a,b or c

[^abc] used to match any character execpt a,b and c

[a-z] used to match character a through z

[A-Z] used to match character A through Z

[0-9] used to match digit 0 through 9

**Metacharacter Inside character**

metacharacter no necessary to escape in Character Set like /h[abc.xyz]t/ matches hat or h.t but doesn't match hot. dot (.) already escaped here no necessary to escaped again   

Except few metacharacter need escape like:
1. ] closing bracket
2. '-' hyphen 
3.  ^ caret 
4.  / escape

**Shorthand for Character Set**

 Shorthand     | Meaning          | Equivalant       |
 ---|---|---|---|
 \d            | Digit            |  [a-zA-Z]        |
 \w            | Word             |  [0-9]           |
 \s            | WhiteSpace       |  [/t/r/n ]       |
 \D            | Not Digit        |  [^a-zA-Z]       |
 \W            | Not Word         |  [^0-9]          |
 \S            | Not WhiteSpace   |  [^/t/r/n ]      |
 
 | Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

