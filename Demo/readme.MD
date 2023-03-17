# Demo
With this demo it is possible to search the database with your own search query. It is not needed to download or install something. Search for **Google Colab** in google search and perform the following.
1. click on the link to google colab wich will open automatically
2. In Google colab, select the GitHub option and copy paste the link to this repository as shown below.
3. Select the document **LIVE_FAIRBattery_QuerySearch.ipynb** ![image](https://user-images.githubusercontent.com/93695286/225937126-42e9180f-1851-49f4-8651-259b2fa44083.png)
4. Enter your personal query. It is important to fill it in exactly as stated in the document. (noted as step 1 in jupter file) 
    + So if you want to search for the query: 

            (word1 & word2 & word3) or (word4) or (word1 & word4)

    + You must enter: 
    
            "word1| AND |word2| AND |word3| OR |word4| OR |word1| AND |word4" 

    ![image](https://user-images.githubusercontent.com/93695286/225937233-6eaa439f-15fb-4624-9fcf-eb446f336284.png)
    put free_search to 'y' if you use words wich are not in the loaded ontology class. If you are restricted by your task to only use ontology terms, put it to 'n'. Some caution is needed if you do that! In the footnote, the default ontology classes are given, copy paste to be sure no typo's will be made. 
5. Select the correct paths to raw data and ontology classes. This is already done, so only needed when you don't go for the default settings. (Noted as step 2 in jupyter file) ![image](https://user-images.githubusercontent.com/93695286/225937438-730245ba-221a-4346-a5e5-2a531e0443d1.png)
6. Press "Runtime" where you select the first option ("Alles uitvoeren") or press "CTRL" + "F9". If the program is not working, press CTRL + F to search for "#!pip install owlready2" remove the hashtag, so it becomes "!pip install owlready2". Again go to Runtime and run all. ![image](https://user-images.githubusercontent.com/93695286/225937329-f0a4268d-35bc-4b59-98d0-dadc887f90e4.png)
7. **!Note!:** the reason to enter queries in this way, avoids us to use SQL, which will make the programm less accesable for non-SQL users. 
8. The keyword data CSV will be generated automatically. To download this file go to the toolbar on the left and click on 'download'. 
![image](https://user-images.githubusercontent.com/93695286/225937587-168028fb-b19b-4ffc-8484-a9dfe4b81c7d.png) ![image](https://user-images.githubusercontent.com/93695286/225937517-21929a9a-60cf-4ad1-8ed4-dd2291055553.png)
9. After you changed your query, press again **run all**. Note that documents may be overwritten!
