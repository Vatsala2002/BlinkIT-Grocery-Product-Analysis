# BlinkIT-Grocery-Product-Analysis
Blinkit is a reputed online grocery store that uses MySQL to analyze their data and make informed, data-driven decisions. By leveraging MySQL, they track sales trends, analyze customer behavior, and identify areas for improvement. For instance, they analyze sales data
for a particular product category or compare sales figures across different outlets to identify areas where they need to focus their
efforts to increase sales. In addition, Blinkit uses MySQL to gather data on customer behavior and preferences. They analyze purchase histories to identify which products are frequently bought together and track customer feedback to gain insights into what their customers are looking for in a grocery store. By utilizing MySQL to analyze their data, Blinkit gains valuable insights into their business operations and makes informed decisions that improve their operations and customer satisfaction. 


In our Case study Blinkit: Grocery Product Analysis, we have a table named 'Grocery Sales' with 12 columns including Item_Identifier,
Item_Weight, Item_Fat_Content, Item_Visibility, Item_Type, Item_MRP, Outlet_Identifier, Outlet_Establishment_Year, Outlet_Size,
Outlet_Location_Type, Outlet_Type and Item_Outlet_Sales. This table contains data on the sales of various grocery items across different
outlets of Blinkit. Using SQL queries in this case study, you'll gain insights into customer behavior and preferences like frequently purchased items, sales trends for specific categories, and customer feedback. These insights will help you improve operations and customer satisfaction, such as increasing sales, improving product offerings based on customer preferences, and enhancing store layout and product placement. 

CODE:

show databases;
use project1;
rename table project1.sql_blinkit_project16875985390 to BLINKIT;
select * from BLINKIT;
#BLINK IT PROJECT	


#2
select Item_Identifier from BLINKIT;

#3
select count(Item_Identifier) from BLINKIT ;

#4
select max(Item_Weight) from BLINKIT;

#5
select min(Item_Weight) from BLINKIT;

#6
select avg(Item_Weight) from BLINKIT;

#7
select count(Item_Fat_Content) from BLINKIT where Item_Fat_Content=('Low Fat');

#8
select count(Item_Fat_Content) from BLINKIT where Item_Fat_Content=('Regular');

#9
select max(Item_MRP) from BLINKIT;

#10
select min(Item_MRP) from BLINKIT;

#11
select Item_Identifier,Item_Fat_Content, Item_Type, Item_MRP from BLINKIT 
where Item_MRP>200;

#12
select max(Item_MRP) from BLINKIT WHERE
Item_Fat_Content=('Low Fat');

#13
select min(Item_MRP) from BLINKIT WHERE
Item_Fat_Content=('Low Fat');

#14
select * from BLINKIT where Item_MRP between 50 and 100;

#15
select distinct Item_Fat_Content from BLINKIT;

#16
select distinct Item_Type from BLINKIT;

#17
select * from BLINKIT order by Item_MRP desc;

#18
select * from BLINKIT order by Item_Outlet_Sales;

#19
select * from BLINKIT order by Item_Type asc;

#20
select Item_Type from BLINKIT where Item_Type in ('dairy','meat');

#21
select distinct Outlet_Size from BLINKIT;

#22
select distinct Outlet_Location_Type 
from BLINKIT;

#23
select distinct Outlet_Type  
from BLINKIT;
---------------
#24
select Item_Type,count(Item_Type) 
from BLINKIT 
group by Item_Type
order by Item_Type desc;

#25
select Outlet_Size,count(Outlet_Size) 
from BLINKIT
group by Outlet_Size
order by Outlet_Size asc;

#26
select Outlet_Type,count(Outlet_Type) 
from BLINKIT
group by Outlet_Type
order by Outlet_Type desc;

#27
select Outlet_Location_Type, count(Outlet_Location_Type)
from BLINKIT
group by Outlet_Location_Type
order by Outlet_Location_Type desc;

#28
select Item_Type,max(Item_MRP) 
from BLINKIT 
group by Item_Type;

#29
select Item_Type,min(Item_MRP) 
from BLINKIT 
group by Item_Type;

#30
select Outlet_Establishment_Year,min(Item_MRP) 
from BLINKIT
group by Outlet_Establishment_Year
order by Outlet_Establishment_Year desc;

#31
select Outlet_Establishment_Year,max(Item_MRP) 
from BLINKIT
group by Outlet_Establishment_Year
order by Outlet_Establishment_Year desc;

#32
select Outlet_Size, avg(Item_MRP) 
from BLINKIT
group by Outlet_Size
order by Outlet_Size desc;

#33
select Outlet_Type,avg(Item_MRP) 
from BLINKIT
group by Outlet_Type
order by Outlet_Type desc;

#34
select Outlet_Type, max(Item_MRP)
from BLINKIT
group by Outlet_Type;

#35
select max(Item_Weight), Item_Type
from BLINKIT
group by Item_Type;

#36
select max(Item_Weight), Outlet_Establishment_Year 
from BLINKIT
group by Outlet_Establishment_Year;

#37
select min(Item_Weight),Outlet_Type 
from BLINKIT
group by Outlet_Type;

#38
select avg(Item_Weight), Outlet_Location_Type
from BLINKIT
group by Outlet_Location_Type
order by Outlet_Location_Type desc;

#39
select max(Item_Outlet_Sales),Item_Type
from BLINKIT
group by Item_Type;

#40
select max(Item_Outlet_Sales),Item_Type
from BLINKIT
group by Item_Type;

#41
select min(Item_Outlet_Sales),Outlet_Establishment_Year 
from BLINKIT
group by Outlet_Establishment_Year;

#42
select max(Item_Outlet_Sales),Outlet_Establishment_Year
from BLINKIT
group by Outlet_Establishment_Year
order by Outlet_Establishment_Year desc;

#43
select avg(Item_Outlet_Sales),Outlet_Size
from BLINKIT
group by Outlet_Size
order by Outlet_Size desc;

#44
select avg(Item_Outlet_Sales), Outlet_Type
from BLINKIT
group by Outlet_Type;

#45
select Outlet_Type, max(Item_Outlet_Sales)
from BLINKIT
group by Outlet_Type;

#46
select sum(Item_Outlet_Sales),Item_Type 
from BLINKIT
group by Item_Type; 

#47
select sum(Item_Outlet_Sales),Item_Fat_Content 
from BLINKIT
group by Item_Fat_Content; 

#48
select max(Item_Visibility),Item_Type 
from BLINKIT
group by Item_Type;

#49
select min(Item_Visibility),Item_Type 
from BLINKIT
group by Item_Type;

#50
select sum(Item_Outlet_Sales),Item_Type
from BLINKIT
where Outlet_Location_Type=('Tier 1')
group by Item_Type;

#51
select sum(Item_Outlet_Sales),Item_Type
from BLINKIT
where Item_Fat_Content in ('Low Fat','LF')
group by Item_Type;

