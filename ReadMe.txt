=========================================================================================================

*************PRODUCT STORE MANAGEMENT APPLICATION************

Using ASP.NET WEBFORM- WEB API-Unity Dependency Injection- Rpository pattern- Entity Framework-SQL Server

=========================================================================================================

Pre-requisite Software:

A) Microsoft Visual Studio (>=2017)

B) SQL Server Management Studio (>=2018)

C) .Net Framework (>=4.5)


***Steps To Set Up The Application (ProductZenserWEbAPI)


1) Extract the ProductZensarApp.zip file--> open ProductZensarApp folder.


***** Database Creation****

2) Open the Sql Server Management Studio

3) Execute the queries given in the ProductZensarApp as "1 Database Creation Query" , "2 DDL Query" and "3 Insert Query" in same order/sequence.


***** Application set Up****



4) Open the ProductZenserWEbAPI.sln file by double click. (if it shows any message box, press ok to continue)

5) If SQL Server Management Studio was logged-in (Authentication Mode) by EITHER



   [A] Windows Authenetication:



   set Sql server name to data source=<<LocalHost>> to below connectionstring code block



   <connectionStrings>

      <add name="ProductStoreEntities" connectionString="metadata=res://*/Models.ProductCategory.csdl|res://*/Models.ProductCategory.ssdl|res://*/Models.ProductCategory.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=<<LocalHost>>;initial catalog=ProductStore;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" />

   </connectionStrings>





   	OR





    [B] SQL Server Authentication:

    

     set User ID=<<sa>> as per system's SQL Server log in credential.

     set Password=<<Temp1234>> as per system's SQL Server log in credential.

     set Sql server name to data source=<<LocalHost>> 

     Change the below connectionstring code block as per above parameters.



     <connectionStrings>

	 <add name="ProductStoreEntities" connectionString="metadata=res://*/Models.ProductCategory.csdl|res://*/Models.ProductCategory.ssdl|res://*/Models.ProductCategory.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=DERIW50Z0045;initial catalog=ProductStore;persist security info=True;User ID=<<sa>>; Password=<<Temp1234>>;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" />

     </connectionStrings>



	

6) In Solution Explorer, expand the "ProductZenserWEbAPI" project---> Open the WebConfig file (XML format).



 Replace the above   <connectionStrings>.....</connectionStrings> block with step 5's <connectionStrings>.....</connectionStrings> block--> save the changes.



7) Please confirm the Order of exection of project as:



Go to Solution Explorer-->Right Click on Solution'ProductZenserWEbAPI' (3 projects) -->select  "set Startup projects..."



Common Properties --> Startup project --> Multiple startup Projects (Click on Radio button for this option)



set the order of project as



 Project                    Action

1)ProductZenserWEbAPI       Start

2)ProductZenserCommon       None

3)ProductZensarApp          Start 



8) To build the application,

 Go to Solution Explorer-->Right Click on Solution'ProductZenserWEbAPI' (3 projects) -->Build Solution



9)To Start the project 

Go to tool bar -->click on "Start"



---------------------------------------------------------Functionality Descriptions: ---------------------------------------------------

ProductStore -Category Record (given as home page)- 



At tool bar we get following functionality as:



1. Go To Category 

A. Clear Search- While getting category by Find filters, it will clear all filters and showing all category record. 

 

B. Find- Searching category with given input the textbox. 

 

C. No. Of product(s) Count- Shows no of products under category. By clicking on the count, it shows products related to that category. 

 

D. Delete- Deleting the category. Could not delete if it has products. 

 

E. Add new- We can add new category in the category record. 

 

F.  Edit- Edit the name of category 

  =================================================================

2. Go To Product - All Details of Products 



A. Search- Giving search to filter the records. 

 

B. Show all products- clearing the filters and showing all the product records 

 

C. Delete- Deleting the product record from the product list.  

 =====================================================================

3. Add New Product- To Add new product in the application 



A. Submit: After filling the all the data, we can submit to add new record of product.

 

B. Clear- Clearing all the values of given input for adding products. 



 =====================================================================

4. Update Existing Product-  To update the details of existing product 



A. Update: Given input for the selected product  will be updated. 

 

B. Cancel: Cancelling the update and clearing the values. 



---------------------------------------------- Thank You ----------------------------------------------