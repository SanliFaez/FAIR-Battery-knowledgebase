# Data Management
This folder contains the data management system and dataset of the FAIR battery project. Read below about the zotero articles and patents library on Flow batteries. The process of 'mining' data with the fairbattery ontology is described and the reader is invited to reproduce our results described below. One is free to use our datasets with respect to the licenses on the main page. We explicitly appreciate contributions. 

### Flow Battery Database
In this project around 5000 articles & patents related to flow batteries are collected in a Zotero database. Zotero is an open source tool to help researchers collect and organize their research documents such as articles. The flow battery database is exported as CSV and searched through by using our FAIR battery ontology. Both datasets, **Data_Raw.csv** and **ProcessedData.csv**, are available in this folder.

### Two data sets
+ (i) **Raw data.CSV**, containing item specific information. The CSV contains 87 columns, which are listed below. The column "Abstract Note" is used to process the data.
	+   Type 'FAIR_Battery_Project' in the search area of <https://www.zotero.org/search/type/group>, to see the Zotero folders.
+ (ii) **Processed data.CSV**, containing raw data supplemented with a column for every ontology class in the flow battery ontology. In each column, there is stored whether the specific ontological term is found in the abstract. If so, the sentences in which this 'keyword' is found, is stored. On every entry this is stored as a list, with 'y' or 'n', where the position in the list corresponds the number of the sentence in the abstract.
	+  **Example:** The ontology class "Electrolyte" is found in the abstract of "Tackling capacity fading in vanadium flow batteries with amphoteric membranes" written by "Oldenburg, Fabio J.; Schmidt, Thomas J.; Gubler, Lorenz" with DOI "10.1016/j.jpowsour.2017.09.051". This is stored in the processed data as ['y', 'n', 'n', 'y', 'y', 'y', 'y'], which means that in sentence 1,4,5,6 and 7 of the abstract this keyword has been found. Click on the DOI link, to read the abstract and check this.

### Process raw data with ontology
The abstracts of articles in the raw dataset are searched through on ontology terms from the FAIR battery ontology. This resulted in the processed data file, see figure below. To process the data, the script **DataProcessor.ipynb** is used. See <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement> to download/run python script. 

![image](https://user-images.githubusercontent.com/93695286/225056874-164241a9-e773-4dd7-ace5-edbe8e8fc8b4.png)

**Figure:** The script "DataProcessorNotebook" imports the raw data as a csv and the ontology as a ttl file. After searching the abstracts one stores if a specific ontology class has been found, and if so in which sentences. The resulting dataset is input for the data search engine. 

### How to contribute with new data?
Imagine you have an article on flow batteries and you want it to be in this database. Then there are 3 ways to contribute to this paper. When adding new data, make sure that the DOI, title and abstract note are available. In order of usefulness of the contribution one can do:
+ (i) **Add new data to raw and process,** Ask for a pull request where you added the article specifics in the raw_data.CSV and the new processed_data.CSV after processing the new raw_data.CSV. See the chapter "Collect Data" to learn how to process the data. These addings can be done manually in the CSV document or via the zotero folder.
+ (ii) **Add new data to raw,** Ask for a pull request where you added the article specifics in the raw_data.CSV. This request will be checked, and approved. The approver needs to create a new issue, to process the new raw data or can do it straight away.
+ (iii) **Tip the repository holder,** Open a new issue and add the DOI or link to the webpage of the publisher of the paper. With this, the new data is not added yet, but is on the backlog or the to-do list to add data. Name your issue as "new data item".

! Note that the more useful the contribution, the more steps are needed by the contributor.

### Reproduction & Python instructions
To reproduce the search results with files, there are two options to run the data processor notebook. 
1. **Run script locally** Download the files: 'DataProcessor.ipynb', 'environment.txt' and 'fairbattery.yml' to create an environment with the correct packages. After installing, one can run the python script locally. The processed data will be exported as csv and pickle file automatically in the same folder. See environment.txt for download instructions
2. **Open DataProcessor.ipynb in Google Colab**
    + Open google colab, select the GitHub option and copy paste the link to this repository as shown below. 
    + Press "Runtime" where you select the first option ("Alles uitvoeren") or press **"CTRL"** + **"F9"**. If the program is not working, remove a hashtag in the first block of code so "#!pip install owlready2", becomes "!pip install owlready2". Again go to Runtime and run all. 
    + The processed data CSV will be generated automatically. To download this file go to the toolbar on the left and click on 'download'.
        ![image](https://user-images.githubusercontent.com/93695286/225653216-90920ea7-08f3-4431-8027-18c3e681f628.png)
        ![image](https://user-images.githubusercontent.com/93695286/225652444-a56c912f-66dc-4f35-913e-317a39d3852c.png)
        ![image](https://user-images.githubusercontent.com/93695286/225657059-a7635648-f766-40c3-b569-d44002bcc452.png)
        ![image](https://user-images.githubusercontent.com/93695286/225658938-996f3de5-0995-443b-96fb-7b50c20ecb9b.png)


#### Raw data column names
|'Key' | 'Item Type'| 'Publication Year'| 'Author'| 'Title' | 'Publication Title'| 'ISBN'|'ISSN'|'DOI'|'Url'|'Abstract Note'|'Date'|'Date Added'|'Date Modified'|'Access Date'| 'Pages'|'Num Pages'| 'Issue'| 'Volume'| 'Number Of Volumes'|'Journal Abbreviation'| 'Short Title'| 'Series'| 'Series Number'|'Series Text'| 'Series Title'| 'Publisher'| 'Place'| 'Language'| 'Rights'| 'Type'| 'Archive'| 'Archive Location'| 'Library Catalog'|'Call Number'| 'Extra'| 'Notes'| 'File Attachments'| 'Link Attachments'| 'Manual Tags'| 'Automatic Tags'| 'Editor'| 'Series Editor'|'Translator'| 'Contributor'| 'Attorney Agent'| 'Book Author'| 'Cast Member'| 'Commenter'| 'Composer'| 'Cosponsor'| 'Counsel'|'Interviewer'| 'Producer'| 'Recipient'| 'Reviewed Author'|'Scriptwriter'| 'Words By'| 'Guest'| 'Number'| 'Edition'| 'Running Time'| 'Scale'| 'Medium'| 'Artwork Size'| 'Filing Date'| 'Application Number'| 'Assignee'| 'Issuing Authority'| 'Country'|'Meeting Name'| 'Conference Name'| 'Court'| 'References'| 'Reporter'|'Legal Status'| 'Priority Numbers'| 'Programming Language'| 'Version'|'System'| 'Code'| 'Code Number'| 'Section'| 'Session'| 'Committee'| 'History'| 'Legislative Body'
| :------------ |:---------------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
|Key given by data base manager Zotero | Explanation on type of article or patent, e.g., journal article, conference paper,... | Year of official publication under given DOI | | |||| Unique identifier of this article, used in processed data | Link to website where full article can be downloaded | If available, the abstract of the item is stored here as text, which is used to process the data |  ||||||||||||||||||||||||| Notes manually added in Zotero | |||||||||||||||||||||||||||||||||||||||||||||||||
#### Processed data column names
This contains the raw data columnnames and the ontology classes as column names. Recall the flow battery ontology (is a) :

![image](https://user-images.githubusercontent.com/93695286/224756657-827f7265-866b-468a-b7ce-fe231d4bfdfb.png)

**Or listed** 'Anode', 'Anolyte Tank', 'Aqueous Metal', 'Aqueous Metallic Electrolyte', 'Aqueous Organic', 'Aqueous Organic Electrolyte', 'C U Plate', 'Cathode', 'Catholyte Tank', 'Container', 'Current Collector', 'Daniel Cell', 'Electrolyte', 'End plate', 'Flow Field', 'Gasket', 'Intermediate Plate', 'Long List Redox Flow Batt', 'Membrane', 'Membraneless', 'Non Aqueous Organic', 'Non Aqueous Organic Electrolyte', 'Non Aqueous Organometallic', 'Non Aqueous Organometallic Electrolyte', 'Power density', 'Pump''Pumpless', 'Redox Potential', 'Stack', 'Subcomponent', 'leakages'
