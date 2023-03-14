# !THIS PAGE IS WORK UNDER CONSTRUCTION! FAIR Battery !THIS PAGE IS WORK UNDER CONSTRUCTION!
# !Check spelling!

FAIR = Findable, Accesable, Interoperatable, Reproducable

+ **!!make sure that the whole project is Findable!**
+ **!!make sure that the whole project is Accesable!**
+ **!!make sure that the whole project is Interoperatable!**
+ **!!make sure that the whole project is Reproducable!**

**Python codes click here**
+ Explain what is in the package
+ Explain the environment
+ Refer to conda cheat sheet
+ Show how to build environment to run the codes. 

![Frontpage](https://github.com/hendelhendel/FAIR_Battery/blob/main/FairbatteryGithub.png?raw=true)

## Introduction
The goal of the FAIR battery project is to create an open source knwoldegebase on redox flow batteries (RFB), where knowledge is **F**indable, **A**ccecable, **I**nteroperatable and **R**eproducable. Therefore, it is needed to collect, search and order availble knowledge from papers, articles and patents. On this Github page one can find the *proof of concept* in the form of a simple data base on RFB's and python scripts to process, or search, the data. The proposed end-user of this concept is a researcher on flow batteries, who needs specific information or those who want to share there own knwoldege on RFB's.
By making use of the concept *ontology*, which is created with the help of *BIG-MAP/BattINFO*, the data is structerd. Below an overview of the project is given. By click on the links in the text one can learn in more detail about specific parts of the project. 

The database can be found here <Link to database> while the python script can be downloaded/runned here<Enter link>. *Are you a possible contributer?* read here how to controbute <link>. Can you help us to make this FAIR battery search better than a G**gle search?

This project is funded by the NWO, with funding code : ABCDEFG1234567. The research is done by the Utrecht University: Sanli Faez, Tom Hommes, Danny de wild and Hendrik Snijder. Sintef has helped with the ontology development in this project.
## Ontology
When people talk with eachother, they use words. These words are related to eachother and thogether they form a message. The order in which they are spoken creates context and give a specific meaning to eachoter. Even in the same context words can have different meanings. To concpetualize this process, people created the concept of ontology. "Ontology is a formal explicit description of concepts and their properties and attributes in a domain" [1]. Since human languages are full of ambiguities, such a formal description becomes relevant for computers to understand them. 

For example in the case of written text an ontology is usefull to extract relevant information out of it. Therefore, several disciplines developed standard onotologies to communicate about their study objects, in the form of classification schemes, flow diagrams and other formal structures. These ontological systems are used to exchange and evolve knowledge between experts. This can foster comon understanding in a certain domain and enable (re-)use of knowledge, standardize assumptions and much more.

In this project an ontology on redox flow batteries is created together with "BIG-MAP/BattINFO" <EnterLink>. To learn more about this ontology see <LinkToOntologyFolder>. With this ontology a search machine is created to search a database of articles related to redox flow batteries.
+ Ontology Readme .md
    + What is ontology
    + Elucidation
    + Flow battery ontology classs
    + What is flowbattery
    + Flowbattery ontology
    + Protege incl screen shots
    + Link to Battinfo and where to find 'official' ontology
    + link to wikipedia
    + Give example of ontolgy
    + Why are ontologies relevant?
    + Generate ontology automatically? https://www.openaire.eu/opscidia-ontology-generator

**References,**
[1] N. F. Noy and D. L.MCGuinness, Ontology Development 101: A guide to Creating Your First
Onotolgy. Stanford University. [Online]. 
Available: https://protege.stanford.edu/publications/ontology_development/ontology101-noy-mcguinness.html

## Flow Battery Database
In this project around 5000 articles & patents related to flow batteries are collected in a Zotero database. Zotero is an open source tool to help researchers collect and organize their research documents such as articles. The flow battery database is exported as CSV and searched through by using our FAIR battery ontology. Both datasets are available as data.CSV on this Github Page <InsertLink> as **raw data.csv** and **Processed data.csv**. See <Enter link> to learn more about the data structure.

**------------------- Begin Move to data folder readme ------------------**
+ (i) **Raw data.CSV**, containing item specific information. The CSV contains 87 columns, which are listed below. The column "Abstract Note" is used to process the data.
	+   Type 'FAIR_Battery_Project' in the search area of <https://www.zotero.org/search/type/group>, to see the Zotero folders.
+ (ii) **Processed data.CSV**, containing raw data supplemented with a column for every ontology class in the flow battery ontology. In each column, there is stored whether the specific ontological term is found in the abstract. If so, the sentences in which this 'keyword' is found, is stored. On every entry this is stored as a list, with 'y' or 'n', where the position in the list corresponds the number of the sentence in the abstract.
	+  **Example:** The ontology class "Electrolyte" is found in the abstract of "Tackling capacity fading in vanadium flow batteries with amphoteric membranes" written by "Oldenburg, Fabio J.; Schmidt, Thomas J.; Gubler, Lorenz" with DOI "10.1016/j.jpowsour.2017.09.051". This is stored in the processed data as ['y', 'n', 'n', 'y', 'y', 'y', 'y'], which means that in sentence 1,4,5,6 and 7 of the abstract this keyword has been found. Click on the DOI link, to read the abstract and check this.

#### How to contribute with new data?
Imagine you have an article on flow batteries and you want it to be in this database. Then there are 3 ways to contribute to this paper. When adding new data, make sure that the DOI, title and abstract note are available. In order of usefulness of the contribution one can do:
+ (i) **Add new data to raw and process,** Ask for a pull request where you added the article specifics in the raw_data.CSV and the new processed_data.CSV after processing the new raw_data.CSV. See the chapter "Collect Data" to learn how to process the data. These addings can be done manually in the CSV document or via the zotero folder.
+ (ii) **Add new data to raw,** Ask for a pull request where you added the article specifics in the raw_data.CSV. This request will be checked, and approved. The approver needs to create a new issue, to process the new raw data or can do it straight away.
+ (iii) **Tip the repository holder,** Open a new issue and add the DOI or link to the webpage of the publisher of the paper. With this, the new data is not added yet, but is on the backlog or the to-do list to add data. Name your issue as "new data item".

! Note that the more useful the contribution, the more steps are needed by the contributor.


#### Raw data column names
|'Key' | 'Item Type'| 'Publication Year'| 'Author'| 'Title' | 'Publication Title'| 'ISBN'|'ISSN'|'DOI'|'Url'|'Abstract Note'|'Date'|'Date Added'|'Date Modified'|'Access Date'| 'Pages'|'Num Pages'| 'Issue'| 'Volume'| 'Number Of Volumes'|'Journal Abbreviation'| 'Short Title'| 'Series'| 'Series Number'|'Series Text'| 'Series Title'| 'Publisher'| 'Place'| 'Language'| 'Rights'| 'Type'| 'Archive'| 'Archive Location'| 'Library Catalog'|'Call Number'| 'Extra'| 'Notes'| 'File Attachments'| 'Link Attachments'| 'Manual Tags'| 'Automatic Tags'| 'Editor'| 'Series Editor'|'Translator'| 'Contributor'| 'Attorney Agent'| 'Book Author'| 'Cast Member'| 'Commenter'| 'Composer'| 'Cosponsor'| 'Counsel'|'Interviewer'| 'Producer'| 'Recipient'| 'Reviewed Author'|'Scriptwriter'| 'Words By'| 'Guest'| 'Number'| 'Edition'| 'Running Time'| 'Scale'| 'Medium'| 'Artwork Size'| 'Filing Date'| 'Application Number'| 'Assignee'| 'Issuing Authority'| 'Country'|'Meeting Name'| 'Conference Name'| 'Court'| 'References'| 'Reporter'|'Legal Status'| 'Priority Numbers'| 'Programming Language'| 'Version'|'System'| 'Code'| 'Code Number'| 'Section'| 'Session'| 'Committee'| 'History'| 'Legislative Body'
| :------------ |:---------------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
|Key given by data base manager Zotero | Explanation on type of article or patent, e.g., journal aricle, conference paper,... | Year of official publication under given DOI | | |||| Unique identifier of this article, used in processed data | Link to website where full article can be downloaded | If available, the abstract of the item is stored here as text, which is used to process the data |  ||||||||||||||||||||||||| Notes manually added in Zotero | |||||||||||||||||||||||||||||||||||||||||||||||||
#### Processed data column names
This contains the raw data columnnames and the ontology classes as column names. Recall the flow battery ontology (is a) :

![image](https://user-images.githubusercontent.com/93695286/224756657-827f7265-866b-468a-b7ce-fe231d4bfdfb.png)

**------------------- End Move to data folder readme ------------------**

#### Process raw data with ontology
The abstracts of articles in the raw dataset are searched through on ontology terms in the FAIR battery ontology. This resulted in the processed data file, see figure below. To process the data, the script *DataProcessorNotebook* is used. See <Link> to download/run python script.

![image](https://user-images.githubusercontent.com/93695286/225056874-164241a9-e773-4dd7-ace5-edbe8e8fc8b4.png)

**Figure:** The script "DataProcessorNotebook" imports the raw data as a csv and the ontology as a ttl file. After searching the abstracts one stores if a specific ontology class has been found, and if so in which sentences. The resulting dataset is input for the data search engine below. 

**--- begin Move to data readme---**
+ Explain pyton script data collection
+ Python environment
**--- end Move to data readme---**

## Data Search Engine
	
![image](https://user-images.githubusercontent.com/93695286/225059361-6accd9bf-e2d3-4a30-a400-bbb9daf50f75.png)

**Figure:** The processed data is imported as a pickle file. The search interface notebook launches a search machine where one can enter a search quiry. In the example above, a search on the ontology term electrolyte is done. The 
+ Explain pytho script search egine
+ Python environment
+ Explain PyQt5 and how to add new things

## Add new data
+ How to add new data: Push data CSV, enter new data and pull request. 
## Future visions of project
+ Show ideas of the search egine as concept
+ Explain that full list of ideas is given as 'issues'
  + Create a fansy report page, sorted by chapter. 
  + Make notebooks runable on Github
  + Ranking System: # times keyword is found, Date of publication..?
  + Link with open science badges?
  + Coupling with AS review in ranking sytstem
  + semantic matching
  + seperate screens (SEE PyQt interface desgin)
  + Organise a hackaton
  + what is the ideal methadata?

## User case
There are several ways to use the python script on this web page. In the simplest case, one can use the existing datasets and search throug them by using the created ontology. This results in lists of articles relevant for a specific ontologyclass.
+ Who should use it?
    + Researchers looking for specific, or those who want to share there, information on redox flow batteries.
+ Why use it?
    + This database contains very specific information on flowbattiers, with traditional search eginies it is not straightforward to achieve this information.
+ How to use it?
    + Download the python script "NAME_SEARCH SCRIPT" as described in <Link to folder> and follow the described steps to laucnh it.
    + Search through the database by using the ontology class buttons as keywords or by typing them yourself. 
    + 
+ How does a result look like?
    + <ENTER screenshot of a search>

+ Resolved feedback by user: If this programm is help full for battery researchers differs per researcher. It is important to explain the details of the program and how its made. Discriminate in material calsses such as: electrolyte, different membrane classes. 
+ Open issues by user: See issues 
    + Enter under issues: Energy densitity is an important part
    + Enter as issues: Add battery properties to the keywords or ontology classes. (Energy density, capacity, costs, )
    + Enter as issues: Can this project answer practical questions such as: Is it possible to make a FAIR battery? How cheap can we go? Is the netwerk going to be active? How do you support the software? How do you keep the knowledge updated? Why would people share their knowledge? 


A more creative use is to enter a new data set of articles and/or another ontology.ttl to search new information on different keywords. 



## Inspirational projects
+ PDF-miner
+ Batt info
+ Battery knowledge base
+ Open knowledge maps

## List of used programmes
+ Zotero
+ Protege
+ Python jupyter-notebook
+ Github
+ Batt Info

## Project logbook
+ Biggest challenges along the way

## Acknowledgement & Coworkers & Contributors
+ Sanli Faez, University of Utrecht
+ Hendrik Snijder, University of Utrecht
+ Tom Hommes, Univeristy of Utrecht
+ Danny de Wild, University of Utrecht
+ Simon Clark, Sintef Norway
+ Eibar Flores, Sintef Norway
