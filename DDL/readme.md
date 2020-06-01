create table mytable 
(id string,
name string
)
ROW FORMAT SERDE
'org.apache.hadoop.hive.serde2.OpenCSVSerde'
WITH SERDEPROPERTIES(
  "escapeChar" = "~"
)
STORED AS TEXTFILE
TBLPROPERTIES(
  'skip.header.line.count' = '1'
);
