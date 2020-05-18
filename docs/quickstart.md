# Velosimo Basics

## Accessing Velosimo

To access Velosimo go to [https://connect.velosimo.com](https://connect.velosimo.com) and login using your Velosimo credentials provided.

NOTE: Velosimo will create Velosimo user accounts for the project teams indentified during the initial implemtation. To request a new Velosimo user user the link below.

https://velosimo.atlassian.net/servicedesk/customer/portals

![image](https://user-images.githubusercontent.com/7420659/62161059-e6818600-b304-11e9-9693-8339fa7910ad.png)

Once logged in, the Dashboard screen displays.

![image](https://user-images.githubusercontent.com/7420659/62161118-fef1a080-b304-11e9-8d7f-26108a5b7b93.png)

## Velosimo Tenants

Velosimo is a multi-tenant based platform allowing agencies easy access to multiple tenants. For example standard EPR and Accela integrations will have 2 or 3 tenants; a Dev, Test, and Production tenant that they will have for continuous development and monitoring.

The current tenant you are working in displays on the Dashboard screen in the Tenants card and on the top-right menu next to user login. The screen shot below is displaying the Queen Creek - test tenant. 

![image](https://user-images.githubusercontent.com/7420659/62161214-28aac780-b305-11e9-9cd1-ff5cc4bc275d.png)

## Monitoring Flow Executions

Flow Executions are the runtime executions of the individual API calls Velosimo makes between SeamlessDoc, EPR, Accela and any intergration that you are implementing with Velosimo. Which could be Dropbox, Google Drive, Laserfiche and Sharepoint to help power a SeamlessDoc intergtaion. 

As a Velosimo Administrator this is the primary screen used to monitor,troubleshoot, and detect issues with the Velosimo flow executions. For example, in the screenshot below the Google Drive|Update Application flow "failed" so the would click on the failed flow to see the issue. Failed flows can be re-run if applicable or you can easily identify the issue with indivdual flow and fix the data.

To access the Flow Executions go to the following URL after logging into Velosimo [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).  We recommend bookmarking this URL in your browser as you will access it frequently.

![image](https://user-images.githubusercontent.com/7420659/62161299-5c85ed00-b305-11e9-8d9d-96acf5400c19.png)

### Managing Collections

Collections are a way of grouping several components of the same business logic that may or may not belong to the same namespace. Using collectiosn is the safest and most efficent way to exported/imported configuration from one tenant to another. For example, you can create a collection of configuration enhancements in the dev tenant and move it to test and production tenants after it is tested and validated in Dev without worrying about missing any configuration elements in the enhancements.

Creating a New Collection 

1. Go to Integrations > Collections >  Add New tab.
2. Give the collections a Name and Title. 
3. Select all the applications, algrorithms, flows, events, data types, schemas, custom validators, translators, etc that you want to group in the collection.  
4. Click the Save button. 

![image](https://user-images.githubusercontent.com/7420659/62161356-7f180600-b305-11e9-8d11-baf87f05892e.png)


Exporting Collections

1. Mark the check box next to the collection being exported. 
2. Go to the Select Items menu in the upper right corner, select the Export selected Collections option from the list.

![image](https://user-images.githubusercontent.com/7420659/62161407-9ce56b00-b305-11e9-9abb-b106c84a32af.png)

3. The Export Collection screen displays, select the Translator Basic|JSON Exporter.

![image](https://user-images.githubusercontent.com/7420659/62161459-c0101a80-b305-11e9-9287-2d0d874e7dc6.png)

4. Click the Export button and collection is created. 

4. The Task > Translations page displays the progress of the export and provides a link to the Collection (JSON file) to download once the export is completed. 

Click on the [attachment](https://docs.google.com/a/velosimo.com/document/d/1fBuSdEWyI3NHL_prbVvjawQKdNGbH7EN8xgVwpMpJBA/edit?usp=drive_web), review the json file of the collection. NOTE: Velosimo recommends reviewing all collection files before importing the collection into other tenants.

![image](https://user-images.githubusercontent.com/7420659/62161507-e8981480-b305-11e9-885e-6e622af4afba.png)

Importing Collections

1. Go to Integrations > My Collections, on the Actions tab select Pull Import from the list. 

2. The Pull Import page displays, click the Choose File button and select the JSON file with the Collection you want to import.
3. Click the Pull Import button.

Go to Integrations > My Collections, on the Actions tab select Pull Import from the list.

![Collections_Pull_Import_2019-10-16](https://user-images.githubusercontent.com/7420659/66947797-0d697180-f043-11e9-86cb-9926ea8bf6bb.png)

The Pull Import page displays, click the Choose File button and select the JSON file with the Collection you want to import.
Click the Pull Import button.

![Attaching_Import_2019-10-16](https://user-images.githubusercontent.com/7420659/66948231-d21b7280-f043-11e9-985a-f18cfae53f1f.png)

Add images Collection and Pull Import to quickstart.md

The task has a Status column that displays the status of the task. When it has been completed, it does not mean that all the resources of the collection have already been imported, this checks the collection resources check was terminated against the resources already existing in the tenant to know which resources should be created and which ones should be updated. 

![image](https://user-images.githubusercontent.com/7420659/62161656-3745ae80-b306-11e9-8bdd-d2b9b596309f.png)

![image](https://user-images.githubusercontent.com/7420659/62161687-49275180-b306-11e9-8f1d-050eeae26a24.png)

After you approve the changes that will be made in the tenant when importing the collection, a task will be generated that will show the progress of the action, at the end all the resources of the collection will be in the tenant. 
