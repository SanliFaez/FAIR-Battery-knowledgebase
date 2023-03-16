# Flow Battery Ontology
In this project an ontology on redox flow batteries (RFB) is created with help from "BIG-MAP/BattINFO" [1]. To learn more about the FAIR battery ontology see [2]. With this ontology a search machine is created to generate knowledge on RFB's from a database of articles and patents in Zotero. The ontology is based on a review by Eduardo et al [3].

## Ontology
When people talk with each other, they use words. These words are ordered and together they form a message. The order in which they are spoken creates context and give a specific meaning to individual words. Even in the same context words can have different meanings. To conceptualize this process, people created the concept of ontology. "Ontology is a formal explicit description of concepts and their properties and attributes in a domain" [4]. Since human languages are full of ambiguities, such a formal description becomes relevant for computers to understand them.

For example in the case of written text an ontology is useful to extract relevant information out of it. Therefore, several disciplines developed standard ontologies to communicate about their study objects, in the form of classification schemes, flow diagrams and other formal structures. These ontological systems are used to exchange and evolve knowledge between experts. This can foster common understanding in a certain domain and enable (re-)use of knowledge, standardize assumptions and much more.
To create an ontology, one can use the program protégè or code directly in to python. For this project, protege is used. For a manual see [4]. Ontologies can be created in many other ways, e.g., automatically see [6] for an example. When working with protege, the following terminology is useful.
1. *Ontology*: A formal explicit description of concepts and their properties and attributes in a domain
of discourse.
2. *Class:* A ’concept’ in a discourse, e.g., the class 'white wine’ is a concept in a discourse of wineology.
Sub classes are more specific concepts within a more general concept. In the example, ’dry white
wine’ can be such a subclass of ’white wine’.
3. *Slot:* A slot is a role or property of a class. In the wine example, one can define e.g, the slots ’maker’ or
’year’. Note that slots have values,
4. *Facets:* Restrictions on slots.
5. *Instances:* Specific individuals in a class, e.g., a specific wine in the class of wines.
6. *Elucidation:* A description of a specific concept. It has similarities with a definition, however an elucidation can be ambiguous, while a definition not. 
7. *'haspart':* A relation between non related (sub)classes, to relate different object to each other in order to make an ensemble object. So in the wineology, one can say. the subclass *dry white wine*, 'has part' class *alcohol*. Here 'alcohol' is a class of some ontology on chemical substances. 
8. *'is a':* This is how classes and subclasses are related to each other. So *dry white wine*, 'is a' *white wine*. 

## Flow battery ontology
The ontology of Batt Info, contains more then flow batteries. From Utrecht university and the FAIR Battery project, we contributed to the ontology of Batt Info. Since the flow battery is a special type of battery, with some overlap in parts of other batteries, the classes of the flow battery ontology are interwoven with those of other battery types. So they are spread out over different files in the BATT Info ontology classes. Therefore, we use a separate flow battery ontology in this repository and in our interface/data processing. This is the *FAIR-Battery-ontology.owl* file, which can be found in above. To learn more on flow batteries, please see the flow battery read me here https://github.com/SanliFaez/FAIR-Battery-knowledgebase/blob/main/MoreInformation/Flowbattery.MD.

![image](https://user-images.githubusercontent.com/93695286/224756657-827f7265-866b-468a-b7ce-fe231d4bfdfb.png)
**Figure:** The flow battery ontology. The blue and yellow lines, represent 'is a' and 'has Part' relations between (sub)Classes. The classes ``ActiveParticipant">"Battery" and "ActiveParticipant">"Separator" are adopted from BATTInfo. As an example, in this graph one can see that a full flow battery contains an Anolyte tank, catholyte tank, pump and an electrochemical flow cell. these parts are no subclasses of each other, however they are all subclasses of ActiveParticipants. An individual instance of a full flow battery is a vanadium flow battery. 

## References
[1] <https://github.com/BIG-MAP/BattINFO>

[2] <https://github.com/SanliFaez/FAIR-Battery-knowledgebase/tree/main/Ontology>

[3] Edgar Ventosa, Massimo Guarnieri, Andrea Trovò, Cristina Flox, Rebeca Marcilla, Francesca Soavi, Petr Mazur, Estibaliz Aranzabe, Eduardo Sánchez-Díez, Raquel Ferret. Redox flow batteries: Status and perspective towards sustainable stationary energy storage. Available: https://doi.org/10.1016/j.jpowsour.2020.228804

[4] N. F. Noy and D. L.MCGuinness, Ontology Development 101: A guide to Creating Your First
Ontology. Stanford University. [Online].
Available: https://protege.stanford.edu/publications/ontology_development/ontology101-noy-mcguinness.html

[5] https://en.wikipedia.org/wiki/Ontology_(computer_science) 

[6] https://www.openaire.eu/opscidia-ontology-generator
