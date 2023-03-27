##### I was able to answer only few questions which are on dataset, and I do not have Domain name knowledge of Gaming, So I was not able to answer the question on them

After Checking data set I do not feel we need any prepossessing is not needed, already the data types of fields are also correct

There is only 2 different game versions gate_30 and gate_40, counts of rows for each versions 44700 and 45489 respectively

Total Number of records = 90189

There is no much difference of retention rate, userid counts for both of the versions of game

Primary Key we can consider userid as there are no duplicates in it

###### Please find the ansers below for the assighnment questions 
1. Which tools would you need to build a sustainable data infrastructure and why?
-  We need ETL tool (Which can extract data from anywhere and transform), Data warehouse, Data Lake, Job Orchestration tool.      
- For ETL we can use:
  1. Python Scripts using different Libraries and API's we can build our own ETL process and use Airflow to schedule it and automate it (Why PYTHON because so many API's for it and so many libraries we have for data manipulation and analysis too)
  2. We can use Talend ETL tool which is licensed tool, where we have drag and drop environment, this has one advantage that is even if you do not know coding we can use tool to build ETL job and easy to debug and faster to create Job than writing script for each report.
- Data Lake: To store the Raw data for future use, we can compress the data or change the file formats to parquet and all to reduce size of the data
We can use AWS S3 or GCP GCS, AWS is older in business and GCP is new and cheap sop we can go to either on our needs
- Data Warehouse : Once raw data is loaded into RDBS Tables we can map the data, Add historical data and all there
We can Use BigQuery or RedShift based on we are using GCP or AWS
- Job Orchestration Tool : We can use Airflow as its open source and works well with python
- For Real Time Streaming we can use Apache Kafka or AWS Kinesis

2. What is the overall retention rate for the game? How does this rate differ by game
version?
- Formula I am using is Retention Rate formula used = count(retention_1 = true or retention_1 = true)/total_count_userid * 100
    Retention_count:43752, total_userid_count:90189
	Overall Retention Rate:48.511%
	-> Retention rate is not varying much if we change the version for this data set, Gate_30 Retention Rate:48.90% and Gate_40 Retention Rate:48.125%

3. What is the distribution of game rounds played? How does this distribution differ by
game version?
- Overall Distribution is Left Skewed meaning most of density is where game rounds < 50, and the distribution remains same even if we change the versions 	
	
4. What is the average number of game rounds played before a player makes an in-app
purchase? How does this average differ by game version?
- I was not able to find Purchase column in data set	

5. What is the correlation between the number of game rounds played and retention? Does
this correlation differ by game version?
- The correlation rate between 	sum_gamerounds and 	retention_1 = 0.197603, sum_gamerounds and	retention_7 = 0.279288 which is not so highly related
  and the correlation change if we look based versions 
- For Gate_30  	sum_gamerounds and 	retention_1 = 0.14729, sum_gamerounds and	retention_7 = 0.214284
- For Gate_40     sum_gamerounds and 	retention_1 = 0.380046, sum_gamerounds and	retention_7 = 0.522188 (Comparatively has more correlation rate for Gate_40 version)
	
8. Can you identify any trends or patterns in player behaviour, such as differences in
behaviour by player country, platform, or game version?
- I did not have many columns to analyze the data and provide answers for it
