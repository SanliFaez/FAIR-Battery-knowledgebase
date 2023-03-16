# FAIR Battery knowledgebase
FAIR = Findable, Accessible, Interoperable, Reproducible

Welcome to the repository of the FAIR battery project. This *open science* research line aims to create a knowledge base on flow batteries. This project is funded by the NWO, with funding code : **ABCDEFG1234567**. The research is done by the Utrecht University: Sanli Faez, Tom Hommes, Danny de wild and Hendrik Snijder. Sintef has helped with the ontology development in this project.

Hendrik Snijder March 2023. 

## Introduction
The goal of the FAIR battery project is to create an open source knowledge base on redox flow batteries (RFB), where knowledge is **F**indable, **A**ccecable, **I**nteroperable and **R**eproducible. Therefore, it is needed to collect, search and order available knowledge from papers, articles and patents. On this Github page one can find the *proof of concept* in the form of a simple database on RFB's and jupyter-notebooks to process, or search, the data. The proposed end-user of this concept is a researcher on RFB's, who needs specific information, or those who want to share, knowledge on RFB's.

By making use of the concept *ontology*, which is created with the help of *BIG-MAP/BattINFO*, the data is structured. Below an overview of the project is given. By clicking on the links in the text below one can learn in more detail about specific parts of the project.

![image](https://user-images.githubusercontent.com/93695286/225754209-5d9641d1-9cf4-4016-834a-220d67a3250f.png)
**Figure:** This scheme shows how different parts of the project are related to each other. On the left hand side, the ontology and Zotero database are imported into a jupyter-notebook. The Data is searched on for ontology terms, and stored as a dataframe. In the "DataProcessor" notebook this results in the processed data files, while in the "Processdata_adn_SearchInterface" notebook, the data frame is used to create a graphical user interface. The Notebook "SearchInterface" launches the same interface from the processed data files.

The database can be found here <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement> while the GUI can be downloaded/runned here <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/GUI>. *Are you a possible contributor?* read below how to contribute. Can you help us to make this FAIR battery search better than a G**gle search?

More information on redox flow batteries can be found here https://github.com/SanliFaez/FAIR-Battery-knowledgebase/blob/main/MoreInformation/Flowbattery.MD and future perspectives here https://github.com/SanliFaez/FAIR-Battery-knowledgebase/blob/main/MoreInformation/UserCase%26prospects.MD

## Ontology
When people talk with each other, they use words. These words are related to each other and together they form a message. The order in which they are spoken creates context and gives a specific meaning to them. Even in the same context words can have different meanings. To conceptualize this process, people created the concept of ontology. "Ontology is a formal explicit description of concepts and their properties and attributes in a domain" [1]. Since human languages are full of ambiguities, a formal description becomes relevant for computers to understand them.

For example in the case of written text an ontology is useful to extract relevant information out of it. Therefore, several disciplines developed standard ontologies to communicate about their study objects, in the form of classification schemes, flow diagrams and other formal structures. These ontological systems are used to exchange and evolve knowledge between experts. This can foster common understanding in a certain domain and enable (re-)use of knowledge, standardize assumptions and much more.

In this project an ontology on redox flow batteries is created with help from "BIG-MAP/BattINFO" <https://github.com/BIG-MAP/BattINFO>. To learn more about the FAIR battery ontology see <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Ontology>. With this ontology a search machine is created to search a database of articles related to redox flow batteries [2].

## Flow Battery Database
In this project around 5000 articles & patents related to flow batteries are collected in a Zotero database. Zotero is an open source tool to help researchers collect and organize their research documents such as articles. The flow battery database is exported as CSV and searched through by using our FAIR battery ontology. Both datasets are available as data.CSV on this Github Page <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement> as **Data_Raw.csv** and **ProcessedData.csv**. See the page above to learn more about the data structure.

## Contribute - Add New Data
Do you have or know an article on flow batteries and you want it to be in this database? Then there are 3 ways to contribute to this paper. When adding new data, make sure that the DOI, title and abstract note are available. In order of usefulness of the contribution one can do:
+ (i) **Add new data to raw and process,** Ask for a pull request where you added the article specifics in the raw_data.CSV and the new processed_data.CSV after processing the new raw_data.CSV. See the chapter "Collect Data" to learn how to process the data. These addings can be done manually in the CSV document or via the zotero folder.
+ (ii) **Add new data to raw,** Ask for a pull request where you added the article specifics in the raw_data.CSV. This request will be checked, and approved. The approver needs to create a new issue, to process the new raw data or can do it straight away.
+ (iii) **Tip the repository holder,** Open a new issue and add the DOI or link to the webpage of the publisher of the paper. With this, the new data is not added yet, but is on the backlog or the to-do list to add data. Name your issue as "new data item".

! Note that the option (iii) is the easiest for the contributor.

## GUI - Data Search Engine
To make it possible to search the flow battery data, a search engine is created as a **proof of concept**. There are two notebook files available to use the FAIR Battery search engine. Both will generate a user interface as shown below. For the end-user, this is where ontology comes together with data. See https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/GUI to learn more on how the python scripts work.

## User case
There are several ways to use the python script on this web page. In the simplest case, one can use the existing datasets and search through them by using the created ontology. This results in lists of articles relevant for a specific ontology class. 

**Example** Imagine, you are a RFB developer, and would like to have detailed information on the interaction between membranes and electrolytes. Also you are dubbing over what pump to use in your battery. Therefore you are interested in two types of articles, those where membranes and electrolytes are described and those where pump's are mentioned. You load the GUI, and enter the query: "Membrane| AND |Electrolyte| OR | Pump" by pressing the buttons or typing directly. With a click on the search button, the DOI's of relevant articles are shown together with the sentences from the abstract where the keywords are found. See the figure below for an impression of this process. 

![image](https://user-images.githubusercontent.com/93695286/225378437-8e328fac-2396-4e84-959a-39f1bd9c213d.png)
**Figure:** In this search engine one can search for articles in which specific words are used. These specific words are exactly those, forming the FAIR Battery ontology. By pressing those buttons, one can search through the database and see in which articles these ontological terms are mentioned. By using the "and'' and "or'' button, a search query can be created. Also direct typing of ontological terms is possible.

**As a remark:** Note that this is work in progress. See future visions for more inspiration. See Q&A for more information on user cases and the first round of feedback on the interface. For open issues see issues. 

## Acknowledgement & Co Workers & Contributors
+ Sanli Faez, University of Utrecht
+ Hendrik Snijder, University of Utrecht
+ Tom Hommes, University of Utrecht
+ Danny de Wild, University of Utrecht
+ Simon Clark, Sintef Trondheim, Norway
+ Eibar Flores, Sintef Trondheim, Norway

## References
1. https://github.com/BIG-MAP/BattINFO
2. https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Ontology
3. Edgar Ventosa, Massimo Guarnieri, Andrea Trovò, Cristina Flox, Rebeca Marcilla, Francesca Soavi, Petr Mazur, Estibaliz Aranzabe, Eduardo Sánchez-Díez, Raquel Ferret. Redox flow batteries: Status and perspective towards sustainable stationary energy storage. Available: https://doi.org/10.1016/j.jpowsour.2020.228804
4. N. F. Noy and D. L.MCGuinness, Ontology Development 101: A guide to Creating Your First Ontology. Stanford University. [Online]. Available: https://protege.stanford.edu/publications/ontology_development/ontology101-noy-mcguinness.html
5. https://en.wikipedia.org/wiki/Ontology_(computer_science)
6. https://www.openaire.eu/opscidia-ontology-generator
7. List of used programmes: Zotero, Protege, Python jupyter-notebook, Github, Batt Info
