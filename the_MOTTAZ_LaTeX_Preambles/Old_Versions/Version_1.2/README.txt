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

README

Version: 1.2
Publish Date: 11/10/2015
Publish Location: Tony's Copy.com cloud storage account
How to use: Save the 'preamble.tex' file to your system, then include the line:
\input{/path/to/preamble.tex}
into your TeX document before '\begin{document}'.

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
|   |
|   |=> Include '\coursetitle', '\hwtitle', and '\name' commands to populate the header.
|
|=> Create a library of other preambles like this one for different uses
|   |
|   |=> Homework
|   |
|   |=> Solutions for students
|   |
|   |=> Exam/quiz
|
|=> Redefine page dimensions to be compatible with A4 paper size

####################################################################################################################################################################
####################################################################################################################################################################



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
