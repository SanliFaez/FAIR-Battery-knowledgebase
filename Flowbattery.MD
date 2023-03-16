# Redox Flow Battery
A redox flow battery (RFB) is an electrochemical device to store energy. There are different types of flow batteries. The most typical RFB contains two liquid electrolytes. These are the anolyte and the catholyte, which are stored in tanks. To store or extract energy from this system, the two liquids are pumped through an electrochemical cell, where they are separated by a membrane. Due to electrochemical configurations, they are able to exchange loaded particles. This flow of current will be collected and transferred outside the chemical cell. See https://en.wikipedia.org/wiki/Flow_battery for an explanation on RFB's. See https://doi.org/10.1016/j.jpowsour.2020.228804 for an overview on Flow Batteries. See figures below for explanation on the flow battery and the charging/discharging process. 

Flow batteries are relevant for future energy storage. Since they can be made of non scarce materials, such as Vanadium or Iron, it is expected that RFB's will be extremely cheap and widely available in the future. While their energy density is not too big, they are scalable and can be used to store energy for, e.g, a household or a small hospital. 

On this page https://github.com/SanliFaez/FAIR-Battery/tree/main/docs/Toms_docs, experiments on a standard flow cell are being developed. 

![image](https://user-images.githubusercontent.com/93695286/225764776-872897a4-cbab-4d80-8c48-a548baa58c72.png)
**figure: RFB** A standard RFB. Inside the electrochemical cell, the charging/discharging takes place, depending on the flowdirection. This is only possible when the pumps are switched hence the electrolytes are flowing. When this process is taking place, it can be connected to an electric circuit where it acts as a battery, or as an energy user. The system as a whole, is called a Redox Flow Battery. 


![image](https://user-images.githubusercontent.com/93695286/225764457-645e3592-16bc-4165-9225-807351603d1a.png)
**Figure: (Dis)Charging** The charging and discharging of electrochemical cells. Depending on the process, a side of the cell is called anode or cathode. 

![image](https://user-images.githubusercontent.com/93695286/224756657-827f7265-866b-468a-b7ce-fe231d4bfdfb.png)
**Figure: RFB-Ontology** The flow battery ontology. The blue and yellow lines, represent 'is a' and 'has Part' relations between (sub)Classes. The classes "ActiveParticipant">"Battery" and "ActiveParticipant">"Separator" are adopted from BATTInfo. As an example, in this graph one can see that a full flow battery, contains an Anolyte tank, catholyte tank, pump and an electrochemical flowcell. these parts, are no subclasses of each other, however they are all subclasses of ActiveParticipants. An individual instance of a full flow battery is a vanadium flow battery.
