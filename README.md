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
The goal of the FAIR battery project is to make knowledge on flowbatteries, **F**indable, **A**ccecable, **I**nteroperatable and **R**eproducable. To create such an open source knowledgebase, it is needed to collect, search and order availble knowledge from papers , articles and patents. That is the goal of this Github page.

Here one can find, a simple data base on redox flowbatteries. Furthermore, there are python scripts to process and search this data. The proposed end-user of this project, is a researcher on flow batteries, who needs specific information or want to share there own knwoldege. 

+ Why is FAIR battery search better than G**gle search?
+ How to read this readme 
+ Download instructions

This project is funded by the NWO, with funding code : ABCDEFG1234567. The research is done by the Utrecht University: Sanli Faez, Tom Hommes, Danny de wilde and Hendrik Snijder. Sintef has helped with the ontology development in this project.

## Ontology
This section is based on the ontology development document of protege [1].
+ What is ontology
  + Elucidation
  + When people talk with eachother, they use words to communicate a certain message. These words carry the message and are related to eachother. The order in which they are spoken give a specific meaning to these words and creates a context. In different contextes, words can have a different meaning. Even in the same context words can have different meanings.
  + To concpetualize this process, people created the concept of ontology. "Ontology is a formal explicit description of concepts and their properties and attributes in a domain" [1]. 
  +  For computers it is hard human language. Nevertheless, computers playing a huge part in human communication. 
  + **Ontology**, several disciplines developed standard methodologies to communicate about their study objects, in the form of classification schemes, flow diagrams and other formal structures. These so called ontological systems are used to exchange and evolve knowledge between experts. This can foster common understanding in a certain domain and enable (re-)use of knowledge, standardize assumptions and much more.
+ Flow battery ontology class
In order to work with ontologies will use the following definitions.
+ 
1. Ontology
Ontology is a formal explicit description of concepts and their properties and attributes in a domain
of discourse.
+ What is flowbattery
+ Flowbattery ontology
+ Protege incl screen shots
+ Link to Battinfo and where to find 'official' ontology
+ link to wikipedia
+ Give example of ontolgy
+ Why are ontologies relevant?
+ Generate ontology automatically? https://www.openaire.eu/opscidia-ontology-generator 
+ Onto trans?
+ **Sources**
    + [1] N. F. Noy and D. L.MCGuinness, Ontology Development 101: A guide to Creating Your First
Onotolgy. Stanford University. [Online]. 
Available: https://protege.stanford.edu/publications/ontology_development/ontology101-noy-mcguinness.html

## Flow Battery Database
In this project around 5000 articles & patents related to flow batteries are collected in a Zotero database. Zotero is an open source tool to help researchers collect and organize their research documents such as articles. The flow battery database is exported as CSV and searched through by using our FAIR battery ontology. Both datasets are available as data.CSV on this Github Page <InsertLink> as:
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

## Collect Data/Search with ontology
With the raw data and the ontology one can search the data using the ontology. This is done in the python script, "NAME_SCRIPT".
To open this script one need to, .. 
+ Explain pyton script data collection
+ Python environment
## Search Data egine
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
+ Biggest challenges allong the way

## Acknowledgement & Coworkers & Contributors
+ Sanli Faez, University of Utrecht
+ Hendrik Snijder, University of Utrecht
+ Tom Hommes, Univeristy of Utrecht
+ Danny de Wild, University of Utrecht
+ Simon Clark, Sintef Norway
+ Eibar Flores, Sintef Norway
