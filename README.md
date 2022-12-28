# rgrep

Your project is to complete the implementation of rgrep, our simplified, restricted grep. rgrep is “restricted” in
the sense that the patterns it matches only support a few regular operators (the easier ones). The way rgrep is
used is that a pattern is specified on the command line. rgrep then reads lines from its standard input and prints
them out on its standard output if and only if the pattern “matches” the line. For example, we can use rgrep to
search for lines that contain text file names that are at least 3 characters long (plus the extension) in a file like the
following:

rgrep searches for patterns and prints it 

.(period) Matches any character
+(plus sign) The preceding character may appear 1 or more times (in other words, the preceding character
can be repeated several times in a row).
?(question
mark)
The preceding character may appear between 0 and 1 times (in other words, the preceding
character is optional).
\(backslash) “Escapes” the following character, nullifying any special meaning it has.
So, here are some examples of patterns and the kinds of lines they match.
( An open parenthesis must appear somewhere in the line.
hey+ Matches a line that contains the string “hey” followed by any number (0 or more) of y’s.
str?ing Matches lines that contain the substrings “string” or “sting”, since the “r” is optional..
z.z\.txt Matches lines that contain the substring “zaz.txt”, “zbz.txt”, etc., where the character between the
z’s can be anything, including a period.
