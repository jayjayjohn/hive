### Array in a column
```
date    city    MyTemp
1/2/17  NYC     23.2,54.2,66.2
1/2/17  Boston  52.1,55.6

create table Temperature(date string,city string,MyTemp array<double>) 
row format delimited 
fields terminated by ‘\t’ 
collection items terminated by ‘,’;
```

### map in a column 
```
date    city    MyTemp
1/2/17  NYC     10:23.2,12:54.2,14:66.2
1/2/17  Boston  10:52.1,12:55.6

create table Temperature(date string, city string, MyTemp map<int,double>) 
row format delimited 
fields terminated by ‘\t’ 
collection items terminated by ‘,’;
map keys terminated by ':'

select myTemp[10] from table
```
### Dataset/struct in a column

```
name   desc
Jay    Male,175,160

create table MyBikes(name string, description struct<gender:string,height:float,weight:float>) 
row format delimited 
fields terminated by ‘\t’ 
collection items terminated by ‘,’;

```

