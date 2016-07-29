  __  __       _   _              _    _       _                          _ 
 |  \/  |     | | | |            | |  | |     (_)                        | |
 | \  / | ___ | |_| |_ __ _ ____ | |  | |_ __  ___   _____ _ __ ___  __ _| |
 | |\/| |/ _ \| __| __/ _` |_  / | |  | | '_ \| \ \ / / _ \ '__/ __|/ _` | |
 | |  | | (_) | |_| || (_| |/ /  | |__| | | | | |\ V /  __/ |  \__ \ (_| | |
 |_|  |_|\___/ \__|\__\__,_/___|  \____/|_| |_|_| \_/ \___|_|  |___/\__,_|_|
  _        _______  __   __  _____                          _     _         
 | |      |__   __| \ \ / / |  __ \                        | |   | |        
 | |     __ _| | ___ \ V /  | |__) | __ ___  __ _ _ __ ___ | |__ | | ___    
 | |    / _` | |/ _ \ > <   |  ___/ '__/ _ \/ _` | '_ ` _ \| '_ \| |/ _ \   
 | |___| (_| | |  __// . \  | |   | | |  __/ (_| | | | | | | |_) | |  __/   
 |______\__,_|_|\___/_/ \_\ |_|   |_|  \___|\__,_|_| |_| |_|_.__/|_|\___|   
                                                                            

(Text art credit: http://patorjk.com/software/taag)


INFO:
Version: 1.7
Author: Tony Mottaz
Publish Date: January 26, 2015
Publish Location: Tony's Copy.com cloud storage account


HOW TO USE:
Save the 'preamble.tex' and 'quiz_preamble.tex' files to your system, then include the line:
\input{/path/to/preamble.tex}
	-or-
\input{/path/to/quiz_preamble.tex}
into your TeX document before '\begin{document}'.

For extremely detailed usage information, refer to the 'Usage Guide.pdf' document.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
ABOUT:                                                                                                                                                              |
	As I began my graduate studies in mathematics, I found that there were lots of commands and customizations that would be beneficial to me when I typed my   	|
homeworks. As the size of this preamble grew, I realized that this was becoming quite a beast, and I decided to document my progress. Some of my colleagues became  |
interested in using this preamble, so I decided to share it with them through the cloud. I started keeping track of versions as I continued to update and add to    |
this preamble.                                                                                                                                                      |
	A word of warning: at this point, this is still a very personal project of mine, and the definitions and customizations are suited to my personal tastes.   	|
I hope that the use of this preamble is easy to figure out, and I welcome suggestions for changes/improvement/additions. In the end, I will do what I think is best,|
and the user is free to make whatever changes they want to make to their own copy.                                                                                  |
	Suggestions for changes can be sent to my email address: tmottaz.snare@gmail.com                                                                            	|
                                                                                                                                                                    |
Happy TeXing!                                                                                                                                                       |
                                                                                                                                                                    |
                                                                             ==========                                                                             |
                                                                                                                                                                    |
THANKS:                                                                                                                                                             |
* A special thanks to Aaron Zolotor for his help in the initial progress and development of the preamble. He continues to put up with my ramblings about different  |
	features I want to add, suggests features of his own, and provides very useful feedback.                                                                    	|
* Thanks to Mac Gallagher for sharing with me the preambles he uses. Nearly all of the changes in version 1.5 were due to his input.                                |
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


IMPORTANT NOTES:
* When you obtain a new version, please be sure to read this section as well as the change log below so that you do not miss any important notes or new features.
* Do not alter the order in which packages are loaded. Some packages need to load before others to avoid conflicting definitions.
	(To see one such error, load the 'wasysym' package before 'amssymb')
* The following packages are needed and might not be currently installed by the user:
	* pgfplots version 1.10
	* arydshln
	* greek-fontenc
	* babel-greek
	* cbfonts
	* cbfonts-fd

#####################################################################################################################################################################
#################################################################   GOALS FOR THE FUTURE   ##########################################################################
#####################################################################################################################################################################

|=> Redevelop this collection of commands into a LaTeX document class/package
|   |
|   |=> Create an option for selecting from a few font choices, such as 'Computer Concrete' or 'Stix'
|   |
|   |=> Create an option for different layout schemes, such as the default article or report layout, my layout scheme, or a 'tight' layout scheme with small margins.
|   |  |
|   |  |=> Each scheme should work independent of the chosen paper size (at least letterpaper and A4).
|
|=> Create a library of other preambles like this one for different uses:
|   |
|   |=> Homework
|   |
|   |=> Solutions for students
|   |
|   |=> Exam/quiz
|
|=> Improve the '\signchart' command
|   |
|   |=> Add keyval options to adjust:
|   |   |
|   |   |=> arrow heads
|
|=> Create a \randclosedloop command for creating arbitrary 2-dimensional spaces in tikz pictures.
|
|=> Add a command similar to '\layout' which will print a page of custom commands unique to this preamble.
|
|=> Consider rewriting this README so that the line lengths are shorter. 

#####################################################################################################################################################################
#####################################################################################################################################################################

Change Log for preamble.tex:

1.1
* Created this README file
* Redefined '\headheight' to account for different font size selections
* Changed '\pgfplotsset{compat=1.9}' to '\pgfplotsset{compat=newest}' for simplified backwards compatibility in the future
* Expanded list of symbols/math operators
* Removed '\myfrac'. This was temporarily defined for a specific use, and was not intended for the universal preamble.
* A comprehensive description of how to define a fraction-like object was added in case this is desired in the future.
* 'Goals for the future' was transferred to this README file. I believe this is a more appropriate location for this list.

1.2
* Added more footnote symbols, adjusted code for improved readability
* Avoided potential footnote counter error by having symbols multiply when needed
* 'pdfpages', 'cleveref', 'wasysym', 'needspace', 'lipsum', and 'alphalph' packages added
* Redefined the proof environment so that if only 3 lines or fewer fit on a page, the entire proof will begin on a new page
* Small adjustments to theoremstyle definitions
* Added commands for choosing alternative fonts.
* Improvement of readability

1.3
* Added command '\darktheme' to invert colors on output PDF. This is to reduce eye strain while creating/editing TeX documents.
* Added command '\circled{@}' which places a circle around the argument in inline text.
* Added the 'IMPORTANT NOTES' section to the README file.
* Added command '\signchart{<numbers>}{<string array>}' which generates a sign chart
* Created a working example of this new feature

1.4
* Added commands '\coursetitle{@}', '\hwtitle{@}', and '\myname{@}' to populate the header
* Changed PGFPlots compatability to version 1.10. After some research, I found that leaving the 'compat' variable as 'newest' is not the best idea.
* Added PGFPlots library 'fillbetween' which allows the user to name plots and add a fill color in between two plots
* Added option 'dvipsnames' to 'xcolor' package to allow for the use of the 68 standard colors in dvips
* Needed to load the 'xcolor' package before the 'pgfplots' package to avoid option class (since 'pgfplots' also loads 'xcolor')
* Added the package 'float' for the placement character 'H', which places the figure "here no matter what"
* Redefined page layout dimensions in terms of paper size and text size, so that the user will see a nice layout no matter which page size/text size they choose.
	The layout has been optimized to conform with standard typography guidelines. For 'letterpaper' size and 11pt or 12pt font, the text spans within the
	recommended range of 60-75 characters per line, and at 10pt font the user will see around 75-85 characters per line, which is only slightly outside of
	this recommended range. As part of this adjustment, the margin size was expanded for the added benefit of a more "useful" margin. That is, longer margin
	notes are readable and no longer appear with one or two words per line. Inspiration for this change came from the discussion on this thread:
	http://tex.stackexchange.com/questions/71172/why-are-default-latex-margins-so-big
* Added numbered versions of theorem, lemma, proposition, and corollary environments

1.5
* Switched from the 'enumerate' package to the 'enumitem' package. 'enumitem' offers much more customization options than 'enumerate'.
	The 'enumerate' package was loaded with the 'shortlabels' option, so TeX documents written with previous versions of the preamble are not affected.
* Added the 'tabularx' package for customization options in tabular environments.
* Added the 'arydshln' package for inserting dashed lines in tabluar/array environments.
* Added a new theorem style 'Case' in the same style as 'Definition'.
* Added the package 'array' for further customizations of tabular/array environments. Specifically, we inserted the global commad '\setlength{\extrarowheight}{1pt]'
	to fix the issue of capitol letters touching the horizontal lines in a table/array.
* Added the command '\set{@}' which places the contents inside of automatically scaled curly braces.
* Added the packages 'textgreek' and 'upgreek' for inserting upright greek letters in text mode and math mode, respectively.
* Added the option 'unicode' to the 'hyperref' package so that if greek letters are used in a hyperlink, they will be nicely replaced with their unicode analogs in
	the side panel/contents of the PDF viewer
* Changed the definition of the doublestroke character '\C' using '\renewcommand', since apparently one of these new packages defined that command already.
* Changed the header text to small caps shape.
* Added the 'fancyvrb' package for customizaton of the verbatim environments.
* Added the option 'align = margin' to itemize environments to place item labels in the left margin.
* Created a usage guide which explains LITERALLY EVERYTHING there is to know about this preamble. If you think there is anything it does not cover, let me know ASAP.
* Added commands '\frameddefinitions' and '\framedtheorems'. When put in the preamble of your document, 'definition' and 'theorem/lemma/proposition/corollary'
	environments will be placed inside of a frame.

1.6
* Changed the '\signchart' command so that entering signs is MUCH simpler. New syntax: '\signchart{1,2,3}{+,-,+,-}'
* Added the 'xkeyval' package for creating key-value pairs for macros
* Added key-value options to '\signchart' to change the width of the chart or the height of the symbols, as well as the arrowheads.
* Fixed bug in '\signchart' definition so that there is no limit to the number of characters in a symbol.
* Added command '\paren{@}' which places its contents inside of auto-scaled parentheses.
* Added the ceiling and floor functions using the commands '\ceil{@}' and '\floor{@}'.
* Changed the default font to 'Latin Modern'. This helps to avoid weird typesetting issues.
* Added the command '\cconj{@}' which places a bar over the argument.

1.7
* Fixed top & bottom spacing for the following environments: nthm, nlem, nprop, ncor, thm, lem, prop, cor, defn, exmp, sol, case.
* There is another preamble! This one is for writing quizzes. Look for the 'quiz_preamble.tex' file.
* Redefined '\Re' and '\Im' so that it prints 'Re' and 'Im' instead of the fraktur font variant
* Added math operator '\fun' for the set of all functions
* Added the double stroke character '\H' for the Quaternions/Hamiltonions
* Redefined the '\bar{@}' command to make it slightly wider and auto-scale with the input.
* Removed the '\cconj{@}' command. I believe this to be too specific when '\bar{@}' is intuitive and does the job nicely.
* Added '\cis' operator as shorthand for 'cos _ i sin'
* Added '\Arg' operator for the Principal Argument of a complex number

&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&

Change Log for quiz_preamble.tex:

1.0
* This is the first iteration. Please give me feedback!
