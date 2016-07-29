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
Version: 1.4
Author: Tony Mottaz
Publish Date: December 5, 2015
Publish Location: Tony's Copy.com cloud storage account

HOW TO USE:
Save the 'preamble.tex' file to your system, then include the line:
\input{/path/to/preamble.tex}
into your TeX document before '\begin{document}'.

ABOUT:
	As I began my graduate studies in mathematics, I found that there were lots of commands and customizations that would be beneficial to me when I typed my
homeworks. As the size of this preamble grew, I realized that this was becoming quite a beast, and I decided to document my progress. Some of my colleagues became
interested in using this preamble, so I decided to share it with them through the cloud. I started keeping track of versions as I continued to update and add to
this preamble.
	A word of warning: at this point, this is still a very personal project of mine, and the definitions and customizations are suited to my personal tastes.
I hope that the use of this preamble is easy to figure out, and I welcome suggestions for changes/improvement/additions. In the end, I will do what I think is best,
and the user is free to make whatever changes they want to make to their own copy.
	Suggestions for changes can be sent to my email address: tmottaz.snare@gmail.com

Happy TeXing!

THANKS:
A special thanks to Aaron Zolotor for his help in the initial progress and development of the preamble. He continues to put up with my ramblings about different
features I want to add, suggests features of his own, and provides very useful feedback.

####################################################################################################################################################################
#################################################################   GOALS FOR THE FUTURE   #########################################################################
####################################################################################################################################################################

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
|   |   |
|   |   |=> total width of the chart
|   |   |
|   |   |=> height adjustment of numbers/signs
|   |
|   |=> Make it easier to input the signs/symbols
|
|=> Create a \randclosedloop command for creating arbitrary 2-dimensional spaces in tikz pictures.
|
|=> Include working examples of features/commands that are unique to this preamble.
|
|=> Add a command similar to '\layout' which will print a page of custom commands unique to this preamble.
|
|=> Create documentation similar to what is found on ctan.org.

####################################################################################################################################################################
####################################################################################################################################################################

IMPORTANT NOTES:
* Do not alter the order in which packages are loaded. Some packages need to load before others to avoid conflicting definitions.
	(To see one such error, load the 'wasysym' package before 'amssymb')

Change Log:

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
	recommended range of 60-75 characters per line, and at 10pt font the user will see around 75-80 characters per line, which is only slightly outside of
	this recommended range. As part of this adjustment, the margin size was expanded for the added benefit of a more "useful" margin. That is, longer margin
	notes are readable and no longer appear with one or two words per line. Inspiration for this change came from the discussion on this thread:
	http://tex.stackexchange.com/questions/71172/why-are-default-latex-margins-so-big
* Added numbered versions of theorem, lemma, proposition, and corollary environments
