## Final Project

In this folder you will find:
* The regression analysis final as a .pdf file
* A powerpoint file used in the final presentation
* A data folder containing the datasets used
* A code folder containing the scripts implemented

The final project focused on missing data. The topic of missing data was chosen out 
of interest. While the midterm project also focused on missing data, the final 
project differed, because:
* The final was a collaborative project
* The final elaborated on Rubin's Rules
* The data had a monotone missing pattern
* SAS was used to impute the missing data

Sara and Ganga, two other graduate students helped me with the project. Sara took care
of the section describing multiple imputation and Rubin's rules, while Ganga worked
on the EM Algorithm section. The code and remaining sections were done by myself. Also,
work on the powerpoint slides was divided in the same manner.

The datasets in the data folder hold information on major tennis matches
from 2013. Tennis players were the observations, and the set result variables had the
monotone missing pattern. For example, a player eliminated after set 2 would have
missing values for sets 3, 4 and 5. Other variables were included to regress on the
response variable, final number of games won. The data was saved in .csv format.
More information can be found in the final project paper.

The code folder contains:
* An ExcelVBA script
* A SAS script
* An R script

The Excel VBA script can be copied and pasted
as a module in Excel, then run as a macro. The script takes clears the contents of cells
with the characters 'NA', so the dataset can be better read by SAS. The script was saved
as DataCleanUp_sub.txt.

The SAS script begins with several data steps. Four datasets were created by reading
the .csv files, then dropping variables and merging the datasets. Following the data
steps came the proc steps. PROC MI multiply imputed the missing data, PROC REG fit an
ordinary regression line to each of the multiply imputed datasets and saved results
in a different dataset and finally PROC MIANALYZE pooled together the parameter estimates
from the previous datasets.