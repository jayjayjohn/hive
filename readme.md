```
date    city    MyTemp
1/2/17  NYC     23.2,54.2,66.2
1/2/17  Boston  52.1,55.6

```
create table Temperature(date string,city string,MyTemp array<double>) 
row format delimited 
fields terminated by ‘\t’ 
collection items terminated by ‘,’;
