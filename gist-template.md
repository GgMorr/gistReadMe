# Title "RegEX Email Validation"

A Regular Expression (RegEx) offers a myriad of techniques that allow for searching through a string of text. Such techniques enable the ability to perform validations, advance find-and-replace methods and more. The purpose of this tutorial is to demonstrate how RegEx is used to validate the characters of an email string.

## Summary

Email addresses are often used as part of user authentication enabling access privileges. The ability to effectively validate an email address is vital to authenticating a users credentials. The affiliated code snippet uses a regex search and match function to validate an email address.

Validation steps include:

1. Accessing user input from an html text box form.
2. Creating a regex test method to validate the following criteria:
    a) User name
    b) Domain name
    c) Extension
    > If the criteria matches, then the color turns green.
    > If the criteria does not match, then the color turns red.
3. Use and if/else statement to match the character of an email address.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
Regex components are a group of processes used to accomplish a variety of search tasks. Common components include: 
    
        Matching Specific Characters
        Matching Fixed Strings
        Matching Character Sets
        Evaluating Occurrances
        Matching Information from a Table 
        ... and more.

When validating an email addres a simple search can confirm that the email address has an "@" symbol followed by no whitespaces. A regex componant example would read as follows:

    Example: ^\S+@\S+$

### Anchors
Anchors (^ and $) are used to determine the position of a search engine within a string. The entire regex expression must be placed between the above two symbols as follows:

    Example: ^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$


### Quantifiers
Quantifiers (*, +, ?, {}) are used in a search to match a variety of characters, groups or character classes in a string. They are used to determine the quantity of characters and expressions to match.

### OR Operator
The OR Operator is used to match expressions or characters on either the left or right of the operator. For example, email addresses often utilize both uppercase and lowercase letters. The OR operater can be leveraged respectively to match a character:

    Example: "(g|G)"

### Character Classes
Also known as character sets, character classes instruct a search engine to match only one of many characters. To perform a search, using a character class, match arguments can be placed inside of square brackets as follows:

        Example: [ae] to match the letter "a" in gray or the letter "e" in grey.

### Flags
Content for code expressions are typcially formatted between beginning and ending forward-slashes (/), in lieu of string quotations. Directly following the ending slash are Flags. Flags are used to customize search activities, against words or characters, in order to render a specified result. Two common flag options are Global and Case Insensitive.

    Global
        Allows you to match anywhere within a string.

    Case Insensitive 
        Used in conjunction with the global flag, this option allows for a successful search/match despite uppercase or lowercase characters.


### Grouping and Capturing
Grouping is a search practice that allows you to group multiple characters in various ways. Leveraging specific operators, such as "+" or "|", grouping enables you to perform more specific search patterns. 
    
    Considering an email address with the word "the" in it(Morristhecat@catfood.com). The following regex example can match the upper or lowercase "t", while checking for two or three of the same characters.

        Example: /(T|t){2,3}he/g


Capturing works in conjunction with Groups to search multiple characters as one unit. Characters placed inside of parenthesis will be captured
    
### Bracket Expressions
Bracket expressions allows for a combination of search specifications where multiple characters can be placed inside of a group. A common use for bracket expressions is the ability to search long-range strings within an expression. A long-range example includes searching from "a-z" or "A-Z" using brackets as follows:



### Greedy and Lazy Match
Greedy search methods are known to leverage repetition operators or quantifiers. A greedy method performs an extensive search to match as much as possible, while returning only what is necesssary to satisfy the searh criteria.

    Example: The regex <.+> matches <GC>first</GC> in:
         "This is a <GC>first</GC> example."

A Lazy Match search method is created by adding a "?" after the "+" quantifier in the same expression. This search method only matches as many characters that are needed, one item at a time.  
    
    Example: <.+?>

### Boundaries
Boundaries references the start and end of a respective search. Such boundaries are expressed using the carat regex "^" symbol, which denotes the starting point of a search, while the dollar regex "$" denotes the endpoint.

When validating numbers within an email address, regex symbols can be used as follows:
    
    Example: const caratDollar = /^\d.+\d$/;

### Back-references
Back-references is the process of repeating a match of the same text or matching the same text again. A good example for using the back-reference process is when you are matching the opening/closing tags of an HTML element.The search process will match the opening element bracket to the closing bracket. An example of a back-reference search includes the following:

    Example: <([A-Z] [A-Z0-9]*\b[^>]*>.*?</\1>

### Look-ahead and Look-behind

The look-ahead and look-behind functions increases the ability to use regular expressions. These functions allow you to actions that occurred before or after a desired capture, without actually capturing what you are looking ahead or behind. Specific symbols are used to aid in the search. For example, a function of look-behind is known as "positive" and requires placement inside of a group that begins with a "?", followed by a "<" and an "=". These three symbols signifies a looking behind and matching of words.

## Author

My name is Gigi and currently I am a student of UCLA Extension Coding Bootcamp. My journey as a full stack developer began approximately four months ago, with a goal of working in the field of web and software development. The journey is arduous, but worth it!

GitHub email: https://github.com/GgMorr 

Gist: https://gist.github.com/GgMorr/a456294473242cbb139e066d84b8b1b6/edit
