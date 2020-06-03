# Collections

Inside Velosimo with have collections, as a way to organize a group of elements of an integration, means that Sharepoint collection, Drive collectionetc. 
Depends what you need to use, your tenant will be setting up with the needed collections. 

# Algorithms

Velosimo also has the Algorithms which are pieces of logic selected to execute and chain in order to process data. we store the output of the algorithm on a DataType record (or records if the output is an array).

## Algorithm notifications

Inside the algorithm code, exits some notification points.
This is the way:

`Tenant.notify(message: "unexpected issue")`

when something unexpected appears and should contact us in Slack

