Can you write me a regular expression which checks for phone numbers in different notations?  
It should support

+49 1234 567890  
01234567890  
0 1234 567890  
(0) 1234 567890  
(0 1234) 56 78 90  
And similar formats

---

&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  
Certainly! Here's a regular expression that matches phone numbers in different notations:

```
^(\+\d{1,3}\s?)?(\()?\d{1,4}(\))?\s?\d{2,4}\s?\d{2,4}\s?\d{2,4}$
```

Let's break down the regex:

- ^ and $ match the start and end of the string, respectively, ensuring that the entire string is matched.
- (\+\d{1,3}\s?)? matches an optional country code in the format "+XX " (where XX is 1 to 3 digits) followed by an optional whitespace character.
- (\()? matches an optional opening parenthesis.
- \d{1,4} matches 1 to 4 digits for the area code or the first part of the phone number.
- (\))? matches an optional closing parenthesis.
- \s? matches an optional whitespace character.
- \d{2,4} matches 2 to 4 digits for the second part of the phone number.
- \s? matches an optional whitespace character.
- \d{2,4} matches 2 to 4 digits for the third part of the phone number.
- \s? matches an optional whitespace character.
- \d{2,4} matches 2 to 4 digits for the fourth part of the phone number.
- 
This regular expression should match phone numbers in the formats you mentioned, including variations with parentheses and whitespace.
