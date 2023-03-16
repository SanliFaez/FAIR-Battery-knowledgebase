# !THIS PAGE IS WORK UNDER CONSTRUCTION! FAIR Battery !THIS PAGE IS WORK UNDER CONSTRUCTION!
# !Check spelling!

FAIR = Findable, Accessible, Interoperable, Reproducible

+ **!!make sure that the whole project is Findable!**
+ **!!make sure that the whole project is Accessible!**
+ **!!make sure that the whole project is Interoperable!**
+ **!!make sure that the whole project is Reproducible!**

**Python codes click here**
+ Explain what is in the package
+ Explain the environment
+ Refer to conda cheat sheet
+ Show how to build environment to run the codes.

![Frontpage](https://github.com/hendelhendel/FAIR_Battery/blob/main/FairbatteryGithub.png?raw=true)

## Introduction
The goal of the FAIR battery project is to create an open source knowledge base on redox flow batteries (RFB), where knowledge is **F**indable, **A**ccecable, **I**interoperable and **R**eproducible. Therefore, it is needed to collect, search and order available knowledge from papers, articles and patents. On this Github page one can find the *proof of concept* in the form of a simple database on RFB's and python scripts to process, or search, the data. The proposed end-user of this concept is a researcher on flow batteries, who needs specific information or those who want to share their own knowledge on RFB's.
By making use of the concept *ontology*, which is created with the help of *BIG-MAP/BattINFO*, the data is structured. Below an overview of the project is given. By click on the links in the text one can learn in more detail about specific parts of the project.

The database can be found here <Link to database> while the python script can be downloaded/runned here<Enter link>. *Are you a possible contributor?* read here how to contribute <link>. Can you help us to make this FAIR battery search better than a G**gle search?

This project is funded by the NWO, with funding code : ABCDEFG1234567. The research is done by the Utrecht University: Sanli Faez, Tom Hommes, Danny de wild and Hendrik Snijder. Sintef has helped with the ontology development in this project.

## Ontology
When people talk with each other, they use words. These words are related to each other and together they form a message. The order in which they are spoken creates context and give a specific meaning to them. Even in the same context words can have different meanings. To conceptualize this process, people created the concept of ontology. "Ontology is a formal explicit description of concepts and their properties and attributes in a domain" [1]. Since human languages are full of ambiguities, a formal description becomes relevant for computers to understand them.

For example in the case of written text an ontology is useful to extract relevant information out of it. Therefore, several disciplines developed standard ontologies to communicate about their study objects, in the form of classification schemes, flow diagrams and other formal structures. These ontological systems are used to exchange and evolve knowledge between experts. This can foster common understanding in a certain domain and enable (re-)use of knowledge, standardize assumptions and much more.

In this project an ontology on redox flow batteries is created with help from "BIG-MAP/BattINFO" <https://github.com/BIG-MAP/BattINFO>. To learn more about the FAIR battery ontology see <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Ontology>. With this ontology a search machine is created to search a database of articles related to redox flow batteries [2].

**References**

[1] N. F. Noy and D. L.MCGuinness, Ontology Development 101: A guide to Creating Your First
Ontology. Stanford University. [Online]. 
Available: https://protege.stanford.edu/publications/ontology_development/ontology101-noy-mcguinness.html

[2] Edgar Ventosa, Massimo Guarnieri, Andrea Trovò, Cristina Flox, Rebeca Marcilla, Francesca Soavi, Petr Mazur, Estibaliz Aranzabe, Raquel Ferret.
Redox flow batteries: Status and perspective towards sustainable stationary energy storage,
Available:  https://doi.org/10.1016/j.jpowsour.2020.228804 Eduardo Sánchez-Díez,  

## Flow Battery Database
In this project around 5000 articles & patents related to flow batteries are collected in a Zotero database. Zotero is an open source tool to help researchers collect and organize their research documents such as articles. The flow battery database is exported as CSV and searched through by using our FAIR battery ontology. Both datasets are available as data.CSV on this Github Page <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement> as **Data_Raw.csv** and **ProcessedData.csv**. See the page above to learn more about the data structure.

#### Process raw data with ontology
The abstracts of articles in the raw dataset are searched through on ontology terms in the FAIR battery ontology. This resulted in the processed data file, see figure below. To process the data, the script **DataProcessor.ipynb** is used. See <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement> to download/run python script.

![image](https://user-images.githubusercontent.com/93695286/225056874-164241a9-e773-4dd7-ace5-edbe8e8fc8b4.png)

**Figure:** The script "DataProcessorNotebook" imports the raw data as a csv and the ontology as a ttl file. After searching the abstracts one stores if a specific ontology class has been found, and if so in which sentences. The resulting dataset is input for the data search engine below. 

## Add new data
Imagine you have an article on flow batteries and you want it to be in this database. Then there are 3 ways to contribute to this paper. When adding new data, make sure that the DOI, title and abstract note are available. In order of usefulness of the contribution one can do:
+ (i) **Add new data to raw and process,** Ask for a pull request where you added the article specifics in the raw_data.CSV and the new processed_data.CSV after processing the new raw_data.CSV. See the chapter "Collect Data" to learn how to process the data. These addings can be done manually in the CSV document or via the zotero folder.
+ (ii) **Add new data to raw,** Ask for a pull request where you added the article specifics in the raw_data.CSV. This request will be checked, and approved. The approver needs to create a new issue, to process the new raw data or can do it straight away.
+ (iii) **Tip the repository holder,** Open a new issue and add the DOI or link to the webpage of the publisher of the paper. With this, the new data is not added yet, but is on the backlog or the to-do list to add data. Name your issue as "new data item".

! Note that the option (iii) is the easiest for the contributor.

## Data Search Engine
There are two python files available to use the FAIR Battery search engine. Both will result in a user interface as shown below. For the end-user, this is where ontology comes together with data. See https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/GUI to learn more on how the python scripts work.

![image](https://user-images.githubusercontent.com/93695286/225378437-8e328fac-2396-4e84-959a-39f1bd9c213d.png)
**Figure:** In this search engine one can search for articles in which specific words are used. These specific words are exactly those, forming the FAIR Battery ontology. By pressing those buttons, one can search through the database and see in wich articles these ontological terms are mentioned. By using the "and'' and "or" button, a search query can be created. Also direct typing of ontological terms is possible.

*As a remark*, note that this GUI is made as a proof of concept. Further development is needed to create more impact. In a future version of this interface, the buttons can be moved to a separate screen and exportation of the search results to CSV must be possible. Also text-mining by using the ontology is one of the possibilities.

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


## Future version of the FAIR Battery Interface
A vision of the future FAIR Battery Interface. These ideas are submitted as issues, so that future contributors can work on them.

=
![image](https://user-images.githubusercontent.com/93695286/225376919-10fb6a4d-c313-401b-983e-e74cc3bd9272.png)
![image](https://user-images.githubusercontent.com/93695286/225377004-adbf3ac2-8c64-4fde-a23f-c5a09d5e4cc4.png)

+ Explain that full list of ideas is given as 'issues'
  + Create a fancy report page, sorted by chapter.
  + Make notebooks runnable on Github
  + Ranking System: # times keyword is found, Date of publication..?
  + Link with open science badges?
  + Coupling with AS review in ranking system
  + semantic matching
  + separate screens (SEE PyQt interface design)
  + Organise a hackathon
  + what is the ideal metadata?

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
+ T.B.A.
+ Biggest challenges allong the way

## Acknowledgement & Coworkers & Contributors
+ Sanli Faez, University of Utrecht
+ Hendrik Snijder, University of Utrecht
+ Tom Hommes, Univeristy of Utrecht
+ Danny de Wild, University of Utrecht
+ Simon Clark, Sintef Norway
+ Eibar Flores, Sintef Norway
