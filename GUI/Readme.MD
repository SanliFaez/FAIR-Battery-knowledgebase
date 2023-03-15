# Graphical User Interface

There are two python notebook files available to use the FAIR Battery search engine. Both will result in a user interface as shown below. For the end-user, this is where ontology comes together with data. For both scripts it is needed to install the python packages as described in the fairbattery.yml file.
+ *SearchInterface.ipynb* Uses the processed data. To run this script, you need to download this script and the 
ProcessedData.pickle file from https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Datamanagement . Store both files in the same folder and run SearchInterface.ipynb in Jypyter-notebook.

+ *Processdata_and_SearchInterface.ipynb* Is the easiest file to use. To run this script, you need to download this file and open it in jupyter-notebook. 

![image](https://user-images.githubusercontent.com/93695286/225059361-6accd9bf-e2d3-4a30-a400-bbb9daf50f75.png)
**Figure:** The processed data is imported as a pickle file. The search interface notebook launches a search machine where one can enter a search quiry. In the example above, a search on the ontology term electrolyte is done. The 

![image](https://user-images.githubusercontent.com/93695286/225373381-1555ef72-7684-44fb-b41b-6cf9cee48e47.png)
**Figure:** In this search engine one can search for articles in which specific words are used. These specific words are exactly those, forming the FAIR Battery ontology. By pressing those buttons, one can search through the database and see in wich articles these ontological terms are mentioned. By using the "and'' and "or" button, a search query can be created. Also direct typing of ontological terms is possible.

*As a remark*, note that this GUI is made as a proof of concept. Further development is needed to create more impact. In a future version of this interface, the buttons can be moved to a separate screen and exportation of the search results to CSV must be possible. Also text-mining by using the ontology is one of the possibilities.
