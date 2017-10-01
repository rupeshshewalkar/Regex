

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

 Shorthand     | Meaning          | Equivalent       |
 --------------|:----------------:|-----------------:|
 \d            | Digit            |  [a-zA-Z]        |
 \w            | Word             |  [0-9]           |
 \s            | WhiteSpace       |  [/t/r/n ]       |
 \D            | Not Digit        |  [^a-zA-Z]       |
 \W            | Not Word         |  [^0-9]          |
 \S            | Not WhiteSpace   |  [^/t/r/n ]      |



**POSIX class	Equivalent to	Matches**

Class | Equivalent| meaning
------|:---------:|---------
[:alnum:]|	[A-Za-z0-9]	|digits, uppercase and lowercase letters
[:alpha:]|	[A-Za-z]	|upper- and lowercase letters
[:ascii:]|	[\x00-\x7F]	|ASCII characters
[:blank:] |	[ \t]	|space and TAB characters only
[:cntrl:]|	[\x00-\x1F\x7F]|	Control characters
[:digit:]|	[0-9]|	digits
[:graph:]|	[^[:cntrl:]]|	graphic characters (all characters which have graphic representation)
[:lower:]|	[a-z]|	lowercase letters
[:print:]|	[[:graph] ]|	graphic characters and space
[:punct:] |	[-!"#$%&'()*+,./:;<=>?@[]^_`{\|}~]	|all punctuation characters (all graphic characters except letters and digits)
[:space:] |	[ \t\n\r\f\v]	|all blank (whitespace) characters, including spaces, tabs, new lines, carriage returns, form feeds, and vertical tabs
[:upper:] |	[A-Z]	|uppercase letters
[:word:]|	[A-Za-z0-9_]	|word characters
[:xdigit:]|	[0-9A-Fa-f]	|hexadecimal digits

**Repitation Metacharacters**

Metacharacter| Meaning
:------------:|:--------
 *| Preceding item zero or more times
 +| Preceding item one or more times
 ?| Preceding item zero or one time

**Quantified Repetition **

{min,max} : min and max are integer number

example :   /d\{1,3\} digit containing one or three like 123, 456, 22 

/d\{1\} minimum single digit 

/d\{1,\} minimum single digit and max infinite 
            
            

