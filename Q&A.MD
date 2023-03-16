## Q&A

Here some possible questions and answers on the usercase are given.

+ **What is the user case?**
There are several ways to use the python script on this web page. In the simplest case, one can use the existing datasets and search throug them by using the created ontology. This results in lists of articles relevant for a specific ontologyclass. 

**Example** Imagine, you are a RFB developer, and would like to have detailed information on the interaction between membranes and electrolytes. Also you are doubing over what pump to use in your battery. There fore you are interested in two type of artcles, those where membranes and electrolytes are described and those where pump's are mentioned. You load the GUI, and enter the query: "Membrane| AND |Electrolyte| OR | Pump" by pressing the buttons or typing directly. With a click on the search button, the DOI's of relevant articles are shown together with the sentences from the abstract where the keywords are found. See the figure below for for an impression of this process. 

![image](https://user-images.githubusercontent.com/93695286/225378437-8e328fac-2396-4e84-959a-39f1bd9c213d.png)
**Figure:** In this search engine one can search for articles in which specific words are used. These specific words are exactly those, forming the FAIR Battery ontology. By pressing those buttons, one can search through the database and see in wich articles these ontological terms are mentioned. By using the "and'' and "or" button, a search query can be created. Also direct typing of ontological terms is possible.

**As a remark:** Note that this is work in progress. See future visions for more inspiration. See Q&A for more information on user cases. 
+ **Who should use it?** Flow battery researchers and developers looking for specific, or those who want to share, information on redox flow batteries.
+ **Why use it?** This growing database contains specific information on flowbattiers, with traditional search engines it is not straightforward to achieve this information without an ontology.
+ **How to use it?** Download the jupyter-notebook "Processdata_and_SearchInterface.ipynb" or "SearchInterface.ipynb" as described in <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/GUI> and follow the described steps to launch it.

+ How does the result look like?
    See usercase
    
**What feedback is there already given?**
In a first round of feedback, some questions raised. Solved issues are 
+ Discriminate in material classes such as: electrolytes and different membrane classes.
+ Make it possible to type directly in the search screen.
+ How to contribute?
+ Explain details of how the GUi and the dataset is made
+ Make it stable --> make it reproducible

For open issues: See issues  
