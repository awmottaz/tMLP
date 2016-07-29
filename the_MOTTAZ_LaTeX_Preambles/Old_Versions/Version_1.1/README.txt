MOTTAZ PREAMBLE --- README

Version: 1.1
Publish Date: 10/27/2015
Publish Location: Tony's Copy.com cloud storage account

How to use: Save the 'preamble.tex' file to your system, then include the line:
\input{/path/to/preamble.tex}
into your TeX document before '\begin{document}'.

##############################
#### GOALS FOR THE FUTURE ####
=> Redevelop this collection of commands into a LaTeX document class
   |
   => Create an option for selecting from a few font choices, such as 'Computer Concrete' or 'Stix'

=> Create a library of other preambles like this one for different uses
   |
   => Homework
   => Solutions for students
   => Exam/quiz

=> Add to the list of footnote symbols
   |
   => Implement fix to automatically duplicate symbols: http://tex.stackexchange.com/questions/78221/changing-footnote-symbols
##############################



Change Log:

1.1
* Created the README file
* Adjusted '\headheight' to account for different font size selections
* Changed '\pgfplotsset{compat=1.9}' to '\pgfplotsset{compat=newest}' for simplified backwards compatibility in the future
* Expanded list of symbols/math operators
* Removed '\myfrac'. This was temporarily defined for a specific use, and was not intended for the universal preamble. A comprehensive description of how to define a fraction-like object was added in case this is desired in the future.
* 'Goals for the future' was transferred to this README file. I believe this is a more appropriate location for this list.
