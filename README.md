# OData-Reader
This project was born out of [this](https://github.com/codeforsanjose/Project-Ideas/issues/86) issue posted in project ideas.

What it does is reads the San Jose web service that returns in OData format, converts this into a json object that can than be used for multiple types of data visualizations (Table w/ sortable columns) and then allows the user to download the data in CSV format.

## Example Data

http://api.sanjoseca.gov/OpenDataService.svc/PlanningPermitsDatas?%24format=json&%24filter=Status%20eq%20%2730%27

This links to planning permits returned in JSON format. 

   { "odata.metadata":"http://api.sanjoseca.gov/OpenDataService.svc/$metadata#PlanningPermitsDatas",
   "value":[  
      {  
         "Status":"30",
         "gx_location":"  CITYWIDE   , SAN JOSE CA ",
         "ASSESSORS_PARCEL_NUMBER":null,
         "ZONING":"A",
         "APPLICANT":"Building DIvision, PBCE, City of San Jose Mr James Son",
         "OWNERNAME":"CITY OF SAN JOSE  City Attorney ",
         "ISSUEUSER":"TCHAULE",
         "PROJECTMANAGER":null,
         "FOLDERNUMBER":"2016-132501-PP",
         "FOLDERDESCRIPTION":"Envir Public Projects",
         "FOLDERNAME":"PP16-090",
         "REFERENCEFILE":"PP16-090",
         "SUBDESCRIPTION":"Exempt",
         "WORKDESCRIPTION":null,
         "ISSUEDATE":"2016-09-02T00:00:00",
         "FINALDATE":null,
         "FOLDERRSN":"1684603"
      },.. ]}
      
It returns the api called, with a array of "values" that are all of the planning permits attributed to a certain query result.       
