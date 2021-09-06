Total Ingested restaurants is obtained by using countuniqueifs formula i.e count unique restaurant ids for a given area. Here range will be RIDs, criteria_range is area

Formula:=COUNTUNIQUEIFS(C:C,E:E,H2)

Available : this is obtained by countuniqueifs i.e count all unique restaurants which has the availability as true, for a given area

Formula:=COUNTUNIQUEIFS(C:C,E:E,H2,F:F,"TRUE")

Available>=5: this is obtained by using countifs i.e counts all restaurants for given area from pivot table which has items greater than 4 (two criteria: area and item_count)

Formula: =COUNTIFS('Pivot Table_HYD'!A2:A21,H2,'Pivot Table_HYD'!C2:C21,">4")

![all areas](https://user-images.githubusercontent.com/53168269/132200506-1facdbf8-7b16-4441-9d27-7d0e97152173.JPG)

Next smaller areas clubbed into major areas by summing values of smaller areas

Formula: =VLOOKUP("Gachibowli",HYD!$H$1:$K$23,2,FALSE)+VLOOKUP("Lingampally & Nalagandla",HYD!$H$1:$K$23,2,FALSE)+VLOOKUP("Kondapur",HYD!$H$1:$K$23,2,FALSE)

![Final dashboard](https://user-images.githubusercontent.com/53168269/132201147-50516da0-a6e7-45f6-a640-3fa0e64f44e1.JPG)
