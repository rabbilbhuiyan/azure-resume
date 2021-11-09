# azure-resume
My own azure resume, following [Azure cloud guru project video.](https://www.youtube.com/watch?v=ieYrBWmkfno&t=1380s&ab_channel=ACloudGuru)

# Section 1: Creating project directory
- creating project structure
- create a new github repo and clone it to local machine
- Also clone the [a cloud guru](https://github.com/ACloudGuru-Resources/acg-project-azure-resume-starter) repo to local machine
- copy the front end and back end folder from a cloud guru repo to your own repo
- frontend folder contains the static website
  - create a file called main.js
  - main.js contains visitor counter code

```js
const getVisitCount = () => {
  let count = 30;
  fetch(functionApi).then(response => {
    return response.json()
```

# Section 2: Building the backend
### Setting up Cosmos DB resources
- create our cosmos DB account, database, container and add counter data to the container
  - create Cosmos DB account:


### Setting up Azure Function
- to interact with our Cosmos DB where counter data is stored
- create azure function with VS code locally to azure function extension 
- set up Cosmos DB bindings to the function
 to retreive and update the counter data
    - go to the azure [resources pages](https://docs.microsoft.com/en-us/azure/azure-functions/functions-bindings-cosmosdb-v2)
    - add by installing NuGet package for C#
    - use .NET CLI and copy the command and head over to VS and run the code in backend-api folder
    - add the key-value pair in local.settings.json
    - from cosmos db account, go to key and copy the primary connection string and paste into key-value pair of local.settings.json
  - Add a C# class to describe the counter object: create a new file (Counter.cs) in backend api folder
  - Now add cosmos DB binding: go to GetResumeCounter.cs file
  - run func host start in the termminal to run the function: it will provide a url to check the count number
  - also go to cosmos data base and check the number of count (updated)

  - so our function running locally and can view the counter data in the browser
  - go to local.setting.json to add Host and CORS and run func host start command in terminal
  - then go to frontend main.js and provide the url in functionApi object
  - now open the index.html file and you will see the count time

### Deploying to Azure
  #### Deploy azure function
  - deploy azure function to azure, grab it's url and update javascript code with it

  #### Deploy to Blob container
  - we will deploy our static site to our blob container

  #### Setup Azure CDN
  - we will setup Azure CDN for HTTPS and custom domain support

### Testing locally
- test our Function loccaly and make sure we can view our counter data in the browser and in our website locally
