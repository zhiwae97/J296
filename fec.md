<h1> Data Diary: Presidential Campaign Finance </h1>
  
<p> Below is the data diary of my analysis on the campaign finance of the 1996 Presidential Election. The data I analyzed here is provided by the Federal Election Commissions about donations totaling more than $100,000 to the Republican and Democratic entities backing Bill Clinton and Bob Dole’s presidential campaigns. This data covers the date from January 1995 to December 1996.</p> 

<h2> Cleaning Data </h2>
<p> I firstly imported the data into OpenRefine for examination and cleaning before further analysis. Here's a list of corrections I made based on my own judgement and preferences. I have listed named the data I changed in case corrections are needed in the future.
  
__1. Fixed typo:__
* Start OpenRefine, apply text facet to "City", click cluster-nearest neighbor, browse for inconsistencies and obivous typos
* Changed "NEW YORKROOK" into "NEW YORK" 
* Changed "DANGERFIELD" into "DAINGERFIELD" 
* Changed "BETHELEHEM" into "BETHLEHEM" 
* Changed "SONNEYWALE" into "SUNNEYWALE" 

__2. Deleted duplicated data:__
* In OpenRefine apply customized duplicate facet to "Donor", select true, then apply text facet to date, sort by count, and check all dates that appeared more than once, cross reference with other categories
* Deleted the following 16 rows of data
* _note: the same result can be achieved by using the data-data clean up-remove duplicate function in Google Sheets, it also recognized 16 duplicates_</br>
!['duplicates.JPG', 'List of Data Duplicates'](/Duplicates.JPG)

__3. Export cleaned dataset from OpenRefine and rename .cvs file [CLEANED] Dataset of SOFT100K 95 96.cvs before uploading to Google Sheets.__
* The dataset can be accessed [here](/https://docs.google.com/spreadsheets/d/1I8JNtYbc0HWIwqUC3SruRIoK6FsVyvvVwvCc_57-hmo/edit?usp=sharing).
 
__4. Added zeros to all the zipcodes that are displayed incorrect__
* In Google Sheets, use Format - Number - Custom Number Format - 00000 to make sure all zipcodes are displayed correct
* In Google Sheets, use Format - Number - Plain Text to make sure zip codes are displayed as text instead of having numerical value


## <h2> Generating Questions </h2>
__1. Which industries contributed the most to the Republican and Democratic parties? How much was contributed to each party?__
* I create a pivot table in Google Sheet 
* Set row as "Industry", collumn as "Party", value as "Amount"
* Sort row by "SUM of Amount" and "D" or "R", in Descending order
* The pivot tables below show that the Media/Entertainment ($1,880,000), Public Sector Unions($1,420,000), and Misc Manufacturing & Distributing($1,400,000) industiry contributed the most to the Democratic Party ; Tobacco($2,420,000), Securities & Investments($2,150,000) are the biggests for the Republican Party. However it is worth noting down that local Republican/Conservative branches together are the biggest donors(4,939,000).

!['PivotTable1.1', 'Industries contributed the most to Democratic Party'](/PivotTable1.1.JPG)
!['PivotTable1.2', 'Industries contributed the most to Republican Party'](/PivotTable1.2.JPG)

__2. How much did donors from the Misc. Business sector contribute to the Democratic party? Which donors were based in Miami Lakes, FL?__
* As shown in the previous pivot table, the Misc. Business sector contributed $1,400,000 to the Democratic parties.
* I double clicked on the amount from Misc. Business sector which allows me to see the details of the data. Apply filter and select "FL" shows me the donor based in Miami Lakes, FL., which is "Windmere Corp".
* !['DetailTable2.1', 'Democratic Misc.Business Donors based in Miami Lakes, FL. '](/DetailTable2.1.JPG)

__3.What percentage of the tobacco industry’s donations does Philip Morris account for? How much is it?__
* In pivot table, set row as donor, value as amount, and add a filter of "Industry" and select "Tobacco"
* The following pivot table shows that Philip Morris donated $1,820,000, and the total of tobacco industry is $2,570,000
* Philip Morris accounts for 1,820,000/2,570,000=71% of the tobacco industry's donations.

<h2> Potential Story </h2>

__Describe (in two to three sentences — no need for a detailed story pitch) one potential story from this dataset that you’d find promising if this were a project you were working on.__

* 
