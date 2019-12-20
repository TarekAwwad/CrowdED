# CrowdED : a Crowdsourcing Evaluation Dataset

CrowdED is a crowdsourcing evaluation dataset. It consists of 300K+ contributions collected from 400 workers for 1000+ questions distributed over 500+ tasks. It also contains a declarative profiles for each worker, a self evaluation (1-5 rating) in different knowledge domains and a crowdsource consistency relevance of this profile. Tasks belong to various domains such as sport, fashion, economy, politics etc., and have different types, relevance judgment, data annotation, image labelling etc.

## Data Structure
```
CrowdED
|-- Core : contains the payload of CrowdED
|   |-- Contributions.csv : contains the contributions
|   |-- Workers.csv : contains the worker profiles
|   |-- Ratings.csv : contains the profile ratings
|   `-- Task.zip : contains the task data
|	   |-- [Task_Set_ID]_auto : contains the HITs of the task set
|	   `-- [Task_Set_ID]_desc : contains the task set description data
|-- More : contains additonal data
|   `-- Task_IDs_Dict.csv : a translation dict from structured task ID to numerical ID
`-- Stats : contains statistical plots of CrowdED
    `-- [Stats].png : one file per statistical entry
```

## Data Description

- **Contributions**.csv : contains the contributions
	- **Header** : Worker_ID, Task_ID, Contributions
	- **Note** : Task_ID is numerical, the Task_ID_Dict can be used to retrieve the structured task ID.

- **Workers**.csv : contains the worker profiles
	- **Header** :
		- Worker_ID, Age, Gender, Education_l, Education_d, Work_experience, Work_domain, Country : self explanatory
		- Language_n,Language_o, : native language and other spoken language
		- Interests_1,Interests_2 : two interest entries
		- V_1, V_2, V_3, V_4, V_5, V_6, V_7: self evaluation votes for knowledge in Sport, Technology, Fashion, Natural Sciences, Politics, Social Media and Humanitarian Work respectively.
		- Full_time_worker : [Binary] whether or not the worker is a full time crowdsourcing contributor
		- Version : The order with which the task set were completed
		- Time_to_complete : the time to fill the profile

- **Ratings**.csv : contains the profile ratings
	- The raw file (from Figure Eight) of ratings for all the profiles found in Workers.csv

- **Task**.zip : contains the task data
	- Both files are Javascript dict shaped entries

## References

Temporarily private Figshare, DOI and reference:
- URL: https://figshare.com/s/c03d6b8b0df781b864ff
- Reference to cite:
	- [1] Tarek Awwad, Nadia Bennani, Veronika Rehn-Sonigo, Lionel Brunie and Harald Kosch CrowdED and CREX : Towards 		Easy Crowdsourcing Quality Control Evaluation ADBIS 2019, Bled - Slovenia

	- [2] Tarek AWWAD. 2018. CrowdED : Crowdsourcing Evaluation Dataset. 
