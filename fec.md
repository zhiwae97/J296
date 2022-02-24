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
* The pivot tables below show that the Media/Entertainment ($1,880,000), Public Sector Unions($1,420,000), and Misc Manufacturing & Distributing($1,400,000) industiry contributed the most to the Democratic Party ; Tobacco($2,420,000), Securities & Investments($2,150,000) are the biggests for the Republican Party. However it is worth noting down that local Republican/Conservative branches together are the biggest donors(4,939,000).</br>
!['PivotTable1.1', 'Industries contributed the most to Democratic Party'](/PivotTable1.1.JPG)
!['PivotTable1.2', 'Industries contributed the most to Republican Party'](/PivotTable1.2.JPG)

__2. How much did donors from the Misc. Business sector contribute to the Democratic party? Which donors were based in Miami Lakes, FL?__
* As shown in the previous pivot table, the Misc. Business sector contributed $1,400,000 to the Democratic Party
* I double clicked on the amount from Misc. Business sector which allows me to see the details of the data. Apply filter and select "FL" shows me the donor based in Miami Lakes, FL., which is "Windmere Corp".</br>
!['DetailTable2.1', 'Democratic Misc.Business Donors based in Miami Lakes, FL. '](/DetailTable2.1.JPG)

__3.What percentage of the tobacco industry’s donations does Philip Morris account for? How much is it?__
* In pivot table, set row as donor, value as amount, and add a filter of "Industry" and select "Tobacco"
* The following pivot table shows that Philip Morris donated $1,820,000, and the total of tobacco industry is $2,570,000</br>
!['PivotTable3.1', 'Donors from the tobacco industry and data on their total donations'](/PivotTable3.1.JPG)
* Philip Morris accounts for 1,820,000/2,570,000=71% of the tobacco industry's donations.

<h2> Potential Story </h2>

__Describe (in two to three sentences — no need for a detailed story pitch) one potential story from this dataset that you’d find promising if this were a project you were working on.__

* Headline: _Presidential Election Finance: Who is Betting on Both Horses and Why?_
* Idea: The official Presidential Campaign finance data suggests that a number of donors contribute money to both candidates. While this has been a common practice by many large coporations, it is still worth exploring what are some of the common rationale behind these donors as well as the privilege they get out of such strategic "bets". 
* Preliminary Analysis: 
  1. Create Pivot Table, set row as "Donor", column as "Party", value as "Amount"
  2. Apply filter to both D and R, deselect "blank"
  3. generate the following table which shows the donors who donated to both presidential candidates and the amounts</br>
!['PivotTable4.1', 'Donors who donated to candidates from both Parties'](/PivotTable4.1.JPG)
* Other sources:
  1. Political Science Scholars/Experts/Commentators
  2. Corporation Representatives (or inside sources)
* Interview Questions Examples:
  1. "What is the common rational behind donating to both candidates?"
  2. "How exactly would your(the donors) organization benefit should one candidate win the election?"
  3. "How do you(the donors) decide how much money would be allocated between each candidate?"


<h2> Supplementary Data</h2>
    1. Past Data about donations made to the Republican and Democratic entities backing presidential candidates (Bush v Gore/Kerry; Obama v McCain/Romney; Trump v Clinton; Biden v Trump). These data sets, combined with the current data, should provide more context about how campaign finance donations changed since the mid 1990s to present. Some possible analysis include: changes in the total sum of donation amounts to each Party candidate; changes in the donating patterns of any single donor or sector, etc.</br>
    
    2.Poll statistics by state (or by city if possible) from the same period. Combining poll data together with campaign finance data offers a glimpse into the political orientation of different states. This may leads to stories revealing how public opinion on politics and big political donors influence (or even contradict) each other.



