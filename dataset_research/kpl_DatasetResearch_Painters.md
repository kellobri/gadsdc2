This dataset, The Painters of de Piles, is a standard R dataset.  It is available by loading the library MASS (library(MASS)), where it  is called "painters." 

**Structure**
The dataset contains subjective assessments of the work of 54 painters. It contains 54 records, one for each painter, each with the following 6 fields:
	the painter's last name (character string)
	assessment scores of 4 characteristics of their work on a scale from 0 to 20:
		composition
		drawing
		colour
		expression
	the school to which the painter belongs, coded with a single charachter as follows:
		A: Rennaissance
		B: Mannerist
		C: Seicento
		D: Venetian
		E: Lombard
		F: Sixteenth Century
		G: Seventeenth Century
		H: French

There are no missing values in the dataset. 

**Summary Dataset Stats**
The actual range of scores assigned is 0 to 18 (so de Piles gave no painters the maximum score of 20 for any characteristic); this is also the range for each category. The means and standard deviations for the 4 characteristics and overall are:
Composition, 11.6, 4.0; Drawing, 12.5, 3.4; Color, 10.9, 4.6; Expression, 7.7, 4.8; overall, 10.7, 4.6.


The highest and lowest ranked schools, using the equally weighted averages of scores across categories for each painter and averaging these across painters for each school (e.g., averaging scores over all categories and painters within a school), were: G, Seventeenth Century (12.3, n=7) and R, Sixteenth Century (8.7, n=4).  

**History**
The dataset is drawn from a list of assessments published in 1708 in  "Balance des Peintre" by the French artist and art critic, Roger de Piles (http://en.wikipedia.org/wiki/Roger_de_Piles).  According to this source, de Piles' list included 56 artists (the source lists only 49), while the R dataset lists 54. De Piles was an important critic of his time, emphasizing the use of color in art.  He "introduced the term 'clair-obscur' (Chiaroscuro) to highlight the effect of color in accentuating the tension between light and dark in a painting." (op.cit.) 

**Literature about this Dataset**
While de Piles' rankings were subjective, two interesting modern scholarly papers about his work support his approach.  In "The Balance of Roger de Piles: A Statistical Analysis," authors Studdert-Kennedy and Davenport state, "Significantly, previous writers on de Piles and the other connoissseurs of the time have pointed to his general importance in the objective study of the arts." They go on to examine de Piles' approach to categorize and score qualities that might be considered most subjective, artistic taste, applying statistical techniques to cluster his subjects using his rankings.  Writing in 1974, the authors demonstrate how such clustering techniques might prove useful for categorizing other qualitative information.

In "Taste Endures! The Rankings of Roger de Piles (†1709) and Three Centuries of Art Prices," Kathryn Graddy shows that de Piles' rankings correlate well with contemporary art prices. 

**Dataset Acquisition**
This dataset is included in the R package, datasets.  I clicked on the box for this package in the pagackages tab of the Files, Plots, Packages, and Help pane of R Studio. I then loaded the library and viewed the dataset with the following commands:
> library(MASS)
> painters

I wanted to load the dataset into excel to compare it to Wikipedias list of painters, so I added the package foreign (clicking on that package as I did for datasets package).  I wrote it to excel using:
> write.table(painters,"C:\\Users\\kperez-lopez\\Documents\\GA_dataScience\\2014_07_28_class3\\painters.xls", sep=",").

The stats above were produced using excel.  I need to do this in R.


**References**
1. Studdert-Kennedy, W. G. & Michael Davenport, M. (1974). The Balance of Roger de Piles: A Statistical Analysis, The Journal of Aesthetics and Art Criticism, Vol. 32, No. 4 (Summer, 1974), pp. 493-502 , Published by: Wiley, Article Stable URL: http://www.jstor.org/stable/429364

2. Graddy, K. (2013). Taste Endures! The Rankings of Roger de Piles 
(†1709) and Three Centuries of Art Prices,The Journal of Economic History, Vol. 73, No. 3 (September 2013). © The Economic History Association. All rights reserved. doi: 10.1017/S0022050713000600.

3. Roger de Piles, http://en.wikipedia.org/wiki/Roger_de_Piles



______________________________________________________________________________
( *copied from R Studio Help* )
R Documentation for Painters
painters {MASS}	R Documentation
The Painter's Data of de Piles

**Description**
The subjective assessment, on a 0 to 20 integer scale, of 54 classical painters. The painters were assessed on four characteristics: composition, drawing, colour and expression. The data is due to the Eighteenth century art critic, de Piles.

**Usage**
painters

**Format**
The row names of the data frame are the painters. The components are:

Composition 	Composition score.

Drawing  		Drawing score.

Colour		Colour score.

Expression	Expression score.

School		The school to which a painter belongs, as indicated by a factor level code as follows: "A": Renaissance; "B": Mannerist; "C": Seicento; "D": Venetian; "E": Lombard; "F": Sixteenth Century; "G": Seventeenth Century; "H": French.

**Source**
A. J. Weekes (1986) A Genstat Primer. Edward Arnold.
M. Davenport and G. Studdert-Kennedy (1972) The statistical analysis of aesthetic judgement: an exploration. Applied Statistics 21, 324–333.
I. T. Jolliffe (1986) Principal Component Analysis. Springer.

**References**
Venables, W. N. and Ripley, B. D. (2002) Modern Applied Statistics with S. Fourth edition. Springer.



