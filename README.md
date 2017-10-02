

### **1. Regex**

- Regular Expressions used to match text and digit.
- Regular Expressions is not programming Langauge
- Regular Expressions are Egar to return answer or match
- Regular Expressions are Greedy to return all match which are possible
- online Regex tool 
  https://www.regexpal.com/
  

### **2 Common Regular Expression**

Symbol | Explaination
:-------|:---------:
. |used to match any character execpt newline
^|used to indicate start of the line
$ |used to indicate end of the line
[abc]|used to match character a,b or c
[^abc]|used to match any character execpt a,b and c
[a-z] |used to match character a through z
[A-Z] |used to match character A through Z
[0-9] |used to match digit 0 through 9


### **3 Metacharacter Inside character**
 
metacharacter no necessary to escape in Character Set like /h[abc.xyz]t/ matches hat or h.t but doesn't match hot. dot (.) already escaped here no necessary to escaped again   

Except few metacharacter need escape like:
1. ] closing bracket
2. '-' hyphen 
3.  ^ caret 
4.  / escape

### **4 Shorthand for Character Set**

 Shorthand     | Meaning          | Equivalent       |
 --------------|:----------------:|-----------------:|
 \d            | Digit            |  [a-zA-Z]        |
 \w            | Word             |  [0-9]           |
 \s            | WhiteSpace       |  [/t/r/n ]       |
 \D            | Not Digit        |  [^a-zA-Z]       |
 \W            | Not Word         |  [^0-9]          |
 \S            | Not WhiteSpace   |  [^/t/r/n ]      |



### **5 POSIX class	Equivalent to	Matches**

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

### **6 Repitation Metacharacters**

Metacharacter| Meaning
:------------:|:--------
 *| Preceding item zero or more times
 +| Preceding item one or more times
 ?| Preceding item zero or one time


### **7 Quantified Repetition**

{min,max} : min and max are integer number

example :   /d\{1,3\} digit containing one or three like 123, 456, 22 

/d\{1\} minimum single digit 

/d\{1,\} minimum single digit and max infinite 



### **8 Grouping Metachracters**

`(): used to grouping metacharacters like /(abc)+/ matches abc, abcabc, abcabcabac`


### **9 Alternation Metacharacters**

`| is OR operator like /apple|orange/ matches "apple" or "orange" `
            

### **10 Anchors Expression**

Symbol| Explaination
:-----|:-------------:
^ | used to start of the line
$ | used to end of the line


### **11 Word Boundaries**

Symbol| Explaination
:-----|:-------------:
/b | used to define Word boundaries
/B | used to not define word boundaries

the boundary is based on a couple of conditions. It is the first word character in the entire string, so that's the first boundary you are going to have, and at the end of the string, the very last word character is going to get boundary as well, and then after that, in between those two, every single time that it shifts between a word character, or a non-word character, we're going to have another boundary. Remember, word characters are the capital letters A to Z, lowercase a to z, 0 to 9, and the underscore.

Examples: 

/\b\d+\b/ matches only digit like 1234 or it doesn't match 8778abc, because it is bounded in digit boundary 

### **12 Back references** 

Grouped expressions are captured 
 - Stores the matched portion in parentheses
 - Stores data matched, not expression 
 - Backreferences allow access to captured data 
 - Refer to first backreference with \1 likewise till \9
 
     Example: 
 
     `/<(html)> hello </\1>/ html word captured in \1`
 
 
 - By default in regex, all mentioned  in () parenthesis are captured :
 
   like /(regex)/ regex word are captured for back references
 - Turn off above behaviour, we need write regex using below syntax
   
      `/(?:regex)/`

       `? means "Give this group a different meaning"

       : means " Turn of capturing"`



 



