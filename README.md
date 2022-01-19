# CLT-CMPD-Data-Aggregation
This data aggregation, and the corresponding visualizations were used to support recommendations to the Charlotte FY 2021 Adopted budget. All data sources used can be found linked in the technical report. The full technical report can be found here below. All visualization figures refrenced-and all code that produced the visulizations-are written in python and available in CMPD_AGGREG.

Caleb Watson
Debra Cook
Tony DiCarlantonio
Aavanth Ezhilan
Safa Khalid

Professors Angela Berardinelli and Justin Grandinetti
DTSC 1301
14 October 2021



 A Data Aggregation: Do CMPD Budget Allocations Put Us in a Position to Meet the Annual ission Statement?
Introduction
	The Charlotte-Mecklenburg Police Department (CMPD) mission statement can be found in the City of Charlotte, Adopted FY 2021 Budget, and reads: “The Charlotte-Mecklenburg Police Department builds problem-solving partnerships with residents to prevent the next crime and enhance the quality of life throughout the community, while treating people with fairness and respect” (124). This prompted our research into a full overview of the department budget to determine if it was allocated towards areas trying to achieve the mission statement. When making such determinations, it is important to understand the conceptual constraints and how spending categories might fit such criteria. Any amount of spending in categories outside of the mission statement should be evaluated cautiously, as can be seen with the details provided throughout this report. Additionally, any evidence to support enhanced efforts of implementing the mission statement will be made aware to suggest alternative spending behaviors. Since the following analysis will examine public funds and provide independent recommendations, there will be a close consideration of any potential benefits and harms that may result from this report. 
 
Concepts and Operationalizing
	Before diving into the full budget, we must first determine what supporting the mission statement through budget spending means. There are two main aspects of the statement that we focus on. The first is the effort to build problem solving relationships with residents. The term build suggests that either these relationships are absent or continuously growing. We would like to identify spending categories that show correlation of mutual activities and/or services between the department and residents. Any type of mutual activity or service would demonstrate such a relationship the mission statement seeks to build. Secondly, we consider the aspect of treating people with fairness and respect. This can be defined as behavior that reinforces equality and anti-discrimination. Areas that demonstrate this type of behavior could fall into categories to support the second aspect of the mission. Ideally, we would like to see efforts of spending that do not just demonstrate the behavior, but support and reinforce fairness and respect within the community.
	It should be noted that how we measure these categories in relation to the mission statement is slightly skewed. We understand the importance of logistical spending, which is why there is an emphasis on behavioral spending as much as there is on categorical. In the instances where categories are subject to logistical matters such as operating and personnel expenses, we look to see the behavior. Are the entirety of these funds necessary, or would they be best put to use in additional areas? Is there full transparency of necessity towards these logistical categories, and are all efforts being made to ensure minimal costs? If there is lack of evidence to support logistical needs, as well as inefficient categorical spending to support the CMPD mission, then we believe there to be excess funds available for additional community programs and/or department training that will better fulfill the mission.
	In order to determine if there are excess funds that could be better allocated towards the CMPD mission statement, we have to find data that accurately reflects the concepts in the mission statement we are focusing on. We will be pooling data from the CMPD Budget Report and CMPD Officer Traffic Stops to operationalize the concepts of the mission statement, but before we can begin analyzing the data, drawing conclusions, and making recommendations based on those data supported conclusions, we have to consider the context of our data and whether or not it is “ethical” to use. 

Literature Review
It can be easy to get wrapped up in research and disregard the context of your data, and further overlook the ethical repercussions that could potentially follow incorrect data contextualization. It’s important that we establish a baseline of what data ethics is, and what it is specifically in regards to our research. Data science has  been described as “a new branch of ethics that studies and evaluates moral problems related to data, algorithms, and corresponding practices”(Floridi et al. 1). Floridi and Tadeo recognize the fact that the determining ethics in data science is a multifaceted process, just as data science itself is a multifaceted process. As researchers it is our personal responsibility to constantly shift from the data and information intensive perspective that is required in data science to an ethically focused perspective, because there is going to be some level of ethics involved in every step of our research. From choosing data to analyze, to making conclusions that have been rigorously tested and elevated from a hypothesis to a data supported conclusion, to making morally sound recommendations and courses of action based on these conclusions, .
When selecting the data sets, we knew the budget data set had to be included because it is this that we are proposing recommendations to. The stakeholders in the budget data are mainly the CMPD, as well as taxpayers. Considering any conclusions we make about the budget data directly reflects the allocation of the CMPD budget, and considering our conclusions affect our recommendations taxpayers are affected because it is ultimately the money that they have paid that we will be making recommendations to adjust. Now, when looking at ethical harms there are not very many security and privacy concerns in this data set, considering the budget report data is not very intimate or personally reflective. Vallor, a reputable technology philosopher, states that one of the biggest concerns of privacy and security is when data gets into the hands of the wrong people. It is then we are at risk of experiencing significant “reputational, economic, and emotional harms”(Vallor 10). However, considering this data set is open to the public there is no chance of any such harm. 
The second data set we use is the CMPD Traffic Stop data set, and this data set is much more intimate and raises all of the harms that Vallor warns us of, and heavily involves our data subjects as stakeholders. Bouncing back to Floridi and Taddeo, we are warned that data “often personal, if not sensitive (big data)”(Floridi et al. 2). We find in the circumstance of the CMPD Traffic Stop data set that this data is both personal and sensitive. We had to consider harms to fairness and justice, privacy, and transparency for this data set because the information contained in this data set is very intimate, personal, and directly related to individuals. We will ensure all individuals with numbers significant enough to be seen in data representation WILL be represented, so there will be no harm to fairness. We considered re-identification possible for a privacy harm. For example, a hacker could re-identify the individuals in the data if specific date and time information of each individual traffic stop was provided. However, this information is confidential information withheld by the city, and is therefore a privacy issue out of our control. Finally, to ensure complete transparency in the work we do with the data set, we will be showing the exact algorithms used to display data representations, so if data subjects we’re curious as to how their data was used in our research we can show them exactly how it was used.
After we consider the ethics of our data sets, we consider the ethics of the algorithm that pulls and displays the samples we want to use from the population. “Technologies are not ethically ‘neutral’, for they reflect the values that we ‘bake in’ to them” (Vallor 10) Vallor says that algorithms are not neutral technologies, they will display (and most of the time magnify) the biases that were already present in them. In this case our algorithm will display data that is directly reflective of the CMPD Traffic Stops Data Set, and furthermore magnify any biases within the data set. This is exactly what we will want it to do, show and magnify any biases, and if it so happens that there are no biases in the CMPD traffic stop data then the algorithm will in fact magnify and display this equality. This magnification of already present relationships in the data is exactly what Vallor refers to as “baked in values”. Once our algorithm is developed it will essentially make conclusions for us, considering we will now be able to look at the relationships in the data table displayed directly as graphs.
After we have ensured that our data sets are ethically just to use, and our algorithm is as well, then we proceed to make recommendations based on our data supported conclusions. However, as researchers we must bounce back to an ethically centered focus to ensure we are being morally just in making recommendations. In order to do this we must fully consider our stakeholders that the recommendations effect. The CMPD as a whole will be affected by any recommendations, as it is their budget that is being adjusted. Secondly, the Charlotte Mecklenburg community and its individual citizens will be affected by any recommendations to the CMPD considering the county and its citizens frequently interact with the CMPD. The Charlotte Mecklenburg tax payers are also stakeholders in our recommendations because as stated before, any budget adjustment recommendation will be ultimately dealing with their money that they pay to the state. Our recommendations also affect individual police officers within the CMPD considering that these recommendations are affecting the department in which they are employed, and paid every month under. So changing overall funds allocations could possibly decrease officer pay if the CMPD deems necessary after our recommendations.
Now we have identified who our research study effects, how it affects them, and why we have considered those who are affected. Our next step is moving on to actually analyzing the data, while always keeping in mind the ethically concerned perspective that we may need to switch to when making conclusions later on down the road. 

Data
Charlotte-Mecklenburg Police Department Budget Analysis
Our objective with this budget analysis was to evaluate the CMPD budget to determine if 2021 spending supports the department’s mission statement: “The Charlotte-Mecklenburg Police Department builds problem-solving partnerships with residents to prevent the next crime and enhance the quality of life through the community, while treating people with fairness and respect.”
Method and Findings
We began our budget analysis by reviewing the City of Charlotte Adopted FY 2021 Budget which we will refer to as the published budget for the purposes of this analysis. This document establishes that CMPD is funded by the city’s general fund and accounts for 40.4% or $290,203,220 of this fund (see fig. 1). This document also establishes that CMPD has the largest full-time employee (FTE) allocation of any city department with 2,455.5 FTEs for 2021 (13). Within the published budget itself some discrepancies are noted regarding the CMPD budget. In the summary of revenues, the published revenue for Police Services totals $22,111,687 for 2021 (15); however, in the Police Budget Overview, the published revenue for Law Enforcement Services is $22,494,957 for 2021 (124). This reflects a difference of $383,270 within the same document. Evaluation of revenues is outside the scope of our analysis which is focused on CMPD spending, but this discrepancy prompted the need for evaluation of the accuracy of the published CMPD spending figures.

Fig. 1. General Fund Expenditures; Adopted FY 2021 Budget. City of Charlotte, July 2020 (10)

We used the Budget Report from the Charlotte Open Data Portal published August 20, 2020 which we will refer to as the budget dataset for the purpose of this analysis. From this dataset we extracted all records with department 30 which translates to department name ‘Charlotte-Mecklenburg Police’. We summed the ‘Adopted_Budget’ figures in these records and then subtracted the value listed in the published budget for departmental charges to compare total CMPD expenditures. The published budget value for total CMPD expenditures is $290,203,220 (124). The value calculated for CMPD expenditures from the dataset is $293,220,762 which is a discrepancy of $3,017,542 (see fig. 2.).
We then split the CMPD budget dataset into the published categories of personnel service, operating expense, and capital outlay. We identified personnel expenses as object values beginning with 51, operating expenses as object values beginning with 52, and capital outlay expenses as object values beginning with 53. We summed each category from the budget dataset returning the following results: personnel expenses totaled $250,364,792, operating expenses totaled 43,464,294, and capital outlay expenses totaled $10,000. We compared these values to the published budget and found the only category with a discrepancy was personnel expenses. The personnel expense category accounted for the entire CMPD budget discrepancy amount of $3,017,542 (see fig. 2.).

Fig. 2. Comparison of CMPD expenses between the published budget and the budget dataset

	To validate our calculations, we used the Fire budget as a comparison since it is the next largest portion of General Fund expenses and has the closest FTE count compared to CMPD. Using the same calculations, we found the values for the published budget and the budget dataset were equal for total expenditures and personnel expenditures. We had to make one adjustment for operating expenditures for the fire budget. The fire budget has an additional object value (57) that does not exist in the CMPD dataset. When we included this value in the calculations for fire operating expenses the budget dataset values matched the published budget values. We returned to the CMPD budget to confirm all object values were accounted for in our original calculations and found that our original calculations for the CMPD budget did include all object values. This validated that our calculations appear correct leaving a CMPD budget discrepancy of $3,017,542.
	With that discrepancy noted, we reviewed each of the CMPD spending categories listed in the budget dataset. We calculated the spending totals for each category to attempt to determine what percent of the CMPD budget was allocated in areas that support CMPD’s mission statement. The result of this analysis revealed that there were no specific categories which detail spending for areas mentioned in the mission statement such as community partner building or initiatives to ensure fair and respectful treatment of people (see fig. 3 and 4). We were unable to assess what portion of the CMPD budget was being directed to the areas mentioned in their mission statement.

Fig. 3. CMPD personnel budget categories

Fig. 4. CMPD operational budget categories
	After the analysis of the budget report and we can began to determine whether or not the budget accurately reflects the mission statement, which says  “The Charlotte-Mecklenburg Police Department builds problem-solving partnerships with residents to prevent the next crime and enhance the quality of life through the community, while treating people with fairness and respect.” As shown by the previous bar graphs along with the interpretation of the budget we can see that there is no specific allocation of the budget which will aid in the show of “treating people with fairness and respect” despite that being one of the focal points in the mission of the Charlotte-Mecklenburg Police Department. In order to advise any recommendations to this budget we would need structured data that supports our claim for the addition of a new section in the budget that will lead to better treatment of people that the CMPD comes in contact with. In order to find this data we needed to find a credible data set that had useful information that we could use in our investigation. 
	We ended up using the Officer Traffic Stops dataset which is a part of the Charlotte Open Data Portal, this set is open up to the public. This dataset has 118,742 officer traffic stops total in 2020. Each stop recorded lists the month of stop, reason for stop, officer race, office gender, officer years of service, driver race, driver ethnicity, driver gender, driver age, whether a search was conducted, result of stop, and CMPD Division. With all this data available we can manipulate the data which would help us conclude that a section in the budget for fairness and respect was necessary. Based on the data in the traffic stop dataset, we decided to look into how a driver’s race affected how they were interacted with by the police officer. 
	In order to get valuable and datasets that were useful we used the Pandas data tool within Python to manipulate the data that we needed. First we looked into the data to figure out what sections would be important to extract in order to support our claim. We looked into the drivers’ races that were pulled over. Based on the information that we extracted from the dataset we can see that out of the 118,742 drivers that were stopped,  66,357 were black drivers which make up approximately 55.9% of all drivers stopped. There were also 45,351 drivers who were white and that is around 38.2% of all drivers stopped. Lastly there were 7,034 drivers who were an unknown race or something other than black or white, in this case Asian or Native American (these groups were not included in this specific because of the small proportion in the traffic stop dataset),  and that made up the remaining 5.9% of drivers. This data is shown in a pie chart (figure. 5) which visually shows the distribution of the drivers stopped based on their race.

Fig. 5. Drivers stopped distribution by race

	With this information there is room for viable reasons as to why the drivers were stopped fairly with justification. For many of these drivers there could have been something that they were doing that was the reason for the stop. So next we decided to extract a smaller part of the sample to reduce some margin of error that could occur due to the potential reasons given prior. In order to do this we added the criteria that the driver must have been searched as well. With this new data we gathered we found that there were a total of 6,642 drivers who were stopped and searched. Out of the 6,642 total drivers, 5,197 were black drivers which make up about 78.2% of drivers that were stopped and searched. Next 1,329 white drivers were stopped and searched which make up around 20% of the drivers that were stopped and searched. Lastly there were 116 unknown/other drivers that were stopped and searched which makes up the remaining 1.7% of drivers that were stopped and searched. As we can see in the pie chart below (Figure 6), there is a large disparity between the black drivers and all the other drivers. 
	
	
Fig. 6. Drivers stopped and searched distribution by race

Even with the data is fig. 6, there are still reasons such as probable cause that would lead to the officer pulling over and searching certain drivers regardless of their race. To combat this and to determine fairness we added one more criteria to the dataset. This last criteria we added was the result of the stop, we added that the stop resulted in a verbal warning and not a citation or an arrest. If the driver was left with a verbal warning then that means that they were searched falsely as no further action was taken by the officers. After inputting the criteria into the dataset we found out that this occurred 3,194 times in 2020. Out of the 3,194 times that this occurred, 2,588 were black drivers that were falsely searched and that makes up around 81% of all the people that were stopped, searched, and let off with a verbal warning. White drivers accounted for 567 of the drivers that were falsely searched which equals about 17.8%. 39 unknown/other drivers were falsely searched and that makes up approximately 1.2% of the total. With this pie chart below (Figure 7) we can see that large difference between the races, specifically white and black within drivers that were falsely searched. 


Fig. 7. Drivers stopped, searched, and given a verbal warning distribution by race


	With all these criteria in place we can now make a conclusion from the new data. Based on figure 7 we can see the large gap in drivers who were falsely searched when they are white versus drivers who are black. This would support our original claim that there is a lack of budget allocations for the goal of increasing fairness and respect in the police force. As the chart suggests there is a lack of fairness based on race and seems to be an underlying race bias in the Charlotte Mecklenburg Police Department. With this in mind, additional funding to a new part of the budget could work to combat and train the police force to remove this thought process which would then help to increase the fairness and respect that the police force treats the community with.


Recommendations
	Although The Charlotte-Mecklenburg Police Department's (CMPD) mission statement emphasizes reaching out to the community to promote fairness and respect to the citizens of the Charlotte-Mecklenburg area, the budget report lacks any focus on community outreach. The inadequacy of the CMPD budget addressing citizens' concerns compromises their safety and their trust in the CMPD. Given its immense funding and the discrepancy between its published budget value and the budget value calculated from the data set provided, additional resources should be allocated towards the community. A "community outreach" category in the following CMPD budget report would greatly promote their mission statement and further encourage relation and understanding between citizens and officers.
As previously mentioned, there is an unallocated $3,017,542 from the published CMPD budget. This lack of transparency prompts distrust and insecurity within taxpayers toward the police department. The CMPD should provide a final audit that will detail where the money is going and how it promotes the mission statement to benefit citizens of the Charlotte-Mecklenburg area. This audit would also push the police department to further pivot the focus of their budget towards the community they are protecting.
In the breakdown of traffic stop data, we concluded that an underlying racial bias exists within the CMPD. The conclusion arose from a lack of resources and funding towards eliminating bias and unfairness within CMPD officers approaching citizens of color. Our recommendation is that the CMPD should identify officers that are more likely to pull over people of color without justification and apply funding to mitigate the behavior.  Moreover, partnering with an organization that identifies and provides "fairness training" towards officers of the aforementioned sort will decrease injustice within the department and the community. Likewise, our recommendation would support the CMPD’s mission statement of providing fairness and respect for all citizens without discrepancy according to race.


Works Cited
City of Charlotte. Adopted FY 2021 Budget. July 2020. charlottenc.gov/budget/Pages/default.aspx. Accessed 16 Sept. 2021.
City of Charlotte. Budget Report. Charlotte Open Data Portal, 20 Aug 2020. data.charlottenc.gov/datasets/budget-report/explore. Accessed 16 Sept. 2021.
City of Charlotte. Officer Traffic Stops. Charlotte Open Data Portal, 8 May 2020. https://data.charlottenc.gov/datasets/charlotte::officer-traffic-stops/explore. Accessed 16 Sept. 2021.
Floridi, Luciano, and Mariarosaria Taddeo. “What Is Data Ethics?” Philosophical Transactions of the Royal Society A: Mathematical, Physical and Engineering Sciences, vol. 374, no. 2083, 2016, p. 1., doi:10.1098/rsta.2016.0360. 
Vallor, Shannon. An Introduction to Data Ethics, 2011, p. 10. 



