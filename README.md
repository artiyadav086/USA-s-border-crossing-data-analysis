# USA-s-border-crossing-data-analysis
Libraries used: pandas, numpy, matplotlib, seaborn | dataset: https://data.bts.gov/Research-and-Statistics/Border-Crossing-Entry-Data/keg4-3bc2

</br>
Due to globalization, there has been increase in  cross border migration since last few decades. This recent trend is due to many reasons. But most important of them all is need for better employment opportunities and living conditions. </br>
However, big proportion of migration is illegal. The big portion illegal migrants choose USA as their preferred destination. This can be attributed to USA's big economy, better living conditions, stability, and the penetrable borders through Mexico. </br> </br>
Analysis </br>
------------</br>
The surge in cross border illegal migration which was more or less constant in 20th century, started to increase for USA since the beginning of 2000s and since 2016 it is observing declining trend.</br>
Top 5 vulnerable states are :</br>
* North Dakota</br>
* Washington</br>
* Maine</br>
* Montana</br>
* Texas</br>
</br>
There is no strong correlation between: </br>
* Measure and illegal migration </br>
* Month and illegal migration</br>
</br>
Most affected port is Eastport: </br>
portname (total immigrants)</br>
------------------------------ </br>
Eastport (6186) </br>
Nogales    (3811) </br>
El Paso	(3797) </br>
Buffalo Niagara Falls	(3793) </br>
Champlain Rouses Point	(3783) </br></br>
Recent trend: </br>
--------------</br>
Gradual decline since 2016 has been observed.
</br>
**END**

</br> </br>
Postgres queries used: </br>
------------------------ </br>
-to collect top vulnerable port names </br>
select portname, count(portname) as 'total immigrants' from border_crossing_entry_data group by portname order by count(portname) desc limit 5;
</br>
