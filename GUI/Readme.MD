# Graphical User Interface
To search the database on flow batteries, there are two jupyter-notebooks available. Both will result in a graphic user interface as shown below. For the end-user, this is where ontology comes together with data. For both scripts it is needed to install the python packages as described in the *fairbattery.yml* and *commands to make new environment.txt* files. 

+ *SearchInterface.ipynb* Uses the processed data. To run this script, you need to download this script and the ProcessedData.pickle file from https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement . Store both files in the same folder and run SearchInterface.ipynb in Jypyter-notebook. 

+ *Processdata_and_SearchInterface.ipynb* Is the easiest file to use. To run this script, you need to download this file and open it in jupyter-notebook. If all the packages are installed int he right way, the interface will generate itself by running all cells. 

**Some remarks on the GUI**
+ Since the interface is built with PyQt5, it is not possible to generate it with google Colab.
+ As described in the .yml file, the used packages are: numpy,pandas,time,matplotlib,owlready2,EMMOntoPy,PyQt5,sys. 
+ Note that this GUI is made as a **proof of concept**, hence further development is needed to create more impact. In a future version of this interface, the buttons can be moved to a separate screen and exportation of the search results to CSV must be possible. Also text-mining by using the ontology is one of the possibilities. See issues for some new ideas. 
+ If you have feedback, please create an issue. 

![image](https://user-images.githubusercontent.com/93695286/225059361-6accd9bf-e2d3-4a30-a400-bbb9daf50f75.png)
**Figure:** The processed data is imported as a pickle file. The search interface notebook launches a search machine where one can enter a search query. In the example above, a search on the ontology term electrolyte is done. The 


![image](https://user-images.githubusercontent.com/93695286/225373381-1555ef72-7684-44fb-b41b-6cf9cee48e47.png)
**Figure:** In this search engine one can search for articles in which specific words are used. These specific words are exactly those, forming the FAIR Battery ontology. By pressing those buttons, one can search through the database and see in which articles these ontological terms are mentioned. By using the "and'' and "or'' button, a search query can be created. Also direct typing of ontological terms is possible.

