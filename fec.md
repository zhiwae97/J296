<h1> Data Diary: Presidential Campaign Finance </h1>
  
<p> Below is the data diary of my analysis on the campaign finance of the 1996 Presidential Election. The data I analyzed here is provided by the Federal Election Commissions about donations totaling more than $100,000 to the Republican and Democratic entities backing Bill Clinton and Bob Dole’s presidential campaigns. This data covers the date from January 1995 to December 1996.</p> 

<h2> Cleaning Data </h2>
<p> I firstly imported the data into OpenRefine for examination and cleaning before further analysis. Here's a list of corrections I made based on my own judgement and preferences. I have listed named the data I changed in case corrections are needed in the future.
  
## 1. Fixed typo:
* Start OpenRefine, apply text facet to "City", click cluster-nearest neighbor, browse for inconsistencies and obivous typos
* Changed "NEW YORKROOK" into "NEW YORK" 
* Changed "DANGERFIELD" into "DAINGERFIELD" 
* Changed "BETHELEHEM" into "BETHLEHEM 

## 2. Deleted duplicated data:
* In OpenRefine apply customized duplicate facet to "Donor", select true, then apply text facet to date, sort by count, and check all dates that appeared more than once, cross reference with other categories
* Deleted the following 16 rows of data
* _note: the same result can be achieved by using the data-data clean up-remove duplicate function in Google Sheets, it also recognized 16 duplicates_</br>
!['duplicates.JPG', 'List of Data Duplicates'](/Duplicate.JPG)

## 3. Export cleaned dataset from OpenRefine and rename .cvs file [CLEANED] Dataset of SOFT100K 95 96.cvs before uploading to Google Sheets.
The dataset can be accessed [here](/https://docs.google.com/spreadsheets/d/1I8JNtYbc0HWIwqUC3SruRIoK6FsVyvvVwvCc_57-hmo/edit?usp=sharing).
 
##4. Added zeros to all the zipcodes that are displayed incorrect
* In Google Sheets, use Format - Number - Custom Number Format - 00000 to make sure all zipcodes are displayed correct
* In Google Sheets, use Format - Number - Plain Text to make sure zip codes are displayed as text instead of having numerical value


<h2> Generating Questions </h2>
1. Which industries contributed the most to the Republican and Democratic parties? How much was contributed to each party?
* 
   
<h2> Potential Story </h2>
