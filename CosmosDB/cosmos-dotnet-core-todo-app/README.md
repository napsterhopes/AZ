This sample shows you how to use the Microsoft Azure Cosmos DB service to store and access data from an ASP.NET Core MVC application.
Web application development with ASP.NET Core MVC using Azure Cosmos DB
This sample shows you how to use the Microsoft Azure Cosmos DB service to store and access data from an ASP.NET Core MVC application hosted on Azure App Service or running locally in your computer.

Running this sample in Visual Studio
Before you can run this sample, you must have the following prerequisites:

Visual Studio 2017 (or higher).
An active Azure Cosmos account or the Azure Cosmos DB Emulator - If you don't have an account, refer to the Create a database account article
Clone this repository using Git for Windows (http://www.git-scm.com/), or download the zip file.

From Visual Studio, open the todo.csproj.

In Visual Studio Build menu, select Build Solution (or Press F6).

Retrieve the URI and PRIMARY KEY (or SECONDARY KEY) values from the Keys blade of your Azure Cosmos account in the Azure portal. For more information on obtaining endpoint & keys for your Azure Cosmos account refer to View, copy, and regenerate access keys and passwords if you are going to work with a real Azure Cosmos account.

The default configuration is setup to work with a local Azure Cosmos DB Emulator.
In the appsettings.json file, located in the project root, find Account and Key and replace the placeholder values with the values obtained for your account if you are going to work with a real Azure Cosmos account.

You can now run and debug the application locally by pressing F5 in Visual Studio.

Deploy this sample to Azure in Visual Studio
In Visual Studio Solution Explorer, right-click on the project name and select Publish...

Using the Pick a publish target dialog, select App Service

Either select an existing App Service, or follow the prompts to create new one. Note: If you choose to create a new one, the App Name chosen must be globally unique.

Once you have selected the App Service, click Publish

After a short time, Visual Studio will complete the deployment.

After deployment, go you your Web App in the Azure Portal and make sure to add the App Settings:

CosmosDb:Account: The endpoint for the Azure Cosmos account.
CosmosDb:Key: The key for the Azure Cosmos account.
CosmosDb:DatabaseName: The name of the Azure Cosmos database to use.
CosmosDb:ContainerName: The name of the Azure Cosmos container to use.
For additional ways to deploy this web application to Azure, please refer to the Deploy ASP.NET Core apps to Azure App Service article which includes information on using Azure Pipelines, CLI, and many more.

Running this sample from the .NET Core command line
Before you can run this sample, you must have the following prerequisites:

.NET Core SDK 3.1 or higher
An active Azure Cosmos account or the Azure Cosmos DB Emulator - If you don't have an account, refer to the Create a database account article
Clone this repository using your Git command line, or download the zip file.

Go to the location of the todo.csproj in your command line prompt.

Run dotnet build to restore packages and build the project.

Retrieve the URI and PRIMARY KEY (or SECONDARY KEY) values from the Keys blade of your Azure Cosmos account in the Azure portal. For more information on obtaining endpoint & keys for your Azure Cosmos account refer to View, copy, and regenerate access keys and passwords if you are going to work with a real Azure Cosmos account.

The default configuration is setup to work with a local Azure Cosmos DB Emulator.
In the appsettings.json file, located in the project root, find Account and Key and replace the placeholder values with the values obtained for your account if you are going to work with a real Azure Cosmos account.

You can now run and debug the application locally by running dotnet run and browsing the Url provided by the .NET Core command line.

Deploy this sample to Azure with Visual Studio Code
Install the Visual Studio Code extension.

Sign in to your Azure account.

Click on the Deploy button on the Azure App Service extension.

Select the src folder to deploy.

Select your Azure subscription and whether you want to select an existing Web App or create a new one. Note: If you choose to create a new one, the App Name chosen must be globally unique.

After a short time, Visual Studio Code will complete the deployment.

After deployment, go you your Web App in the Azure Portal and make sure to add the App Settings:

CosmosDb:Account: The endpoint for the Azure Cosmos account.
CosmosDb:Key: The key for the Azure Cosmos account.
CosmosDb:DatabaseName: The name of the Azure Cosmos database to use.
CosmosDb:ContainerName: The name of the Azure Cosmos container to use.
For additional ways to deploy this web application to Azure, please refer to Deploy to Azure using App Service or Deploy to Azure using the Azure CLI.

About the code
The code included in this sample is intended to get you going with a simple ASP.NET Core MVC application that connects to Azure Cosmos DB. It is not intended to be a set of best practices on how to build scalable enterprise grade web applications. This is beyond the scope of this quick start sample.

More information
Azure Cosmos DB Documentation
Azure Cosmos DB .NET SDK
Azure Cosmos DB .NET SDK Reference Documentation
