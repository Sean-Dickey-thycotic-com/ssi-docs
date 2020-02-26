[title]: # (Create a Token)
[tags]: # (token)
[priority]: # (202)
[display]: # (none)
# How to Create a Token

## Create a new Project

<!-- add information on how to verify that the integration works -->

1. Open UiPath Studio console.

   ![Orchestrator Settings](images/17.png)
1. Click __Process__ to start a new project.

   ![Orchestrator Settings](images/18.png)
1. Enter in a name and description for the project.
1. Click __Create__.

   ![Orchestrator Settings](images/19.png)
1. Click on the __Project__ folder.
1. Click on __New__ and __sequence__.

   ![Orchestrator Settings](images/20.png)
1. Name the new sequence and click __Create__.

   ![Orchestrator Settings](images/21.png)
1. The following screen will appear.

   ![Orchestrator Settings](images/22.png)

## How to Create a Token

1. Click on __Manage Packages__.

   ![Orchestrator Settings](images/23.png)
1. Select __All Packages__.
1. Search for __webapi__.
1. Click on __UiPath.Web.Activities__.

   ![Orchestrator Settings](images/24.png)
1. Click __Install__ and __Save__.
1. Search for _HTTP Request__ in the project console.

   ![Orchestrator Settings](images/25.png)
1. Drag and drop the _HTTP Request__ to the sequence name (Example: tokenGet).

   ![Orchestrator Settings](images/26.png)
1. In the __HTTP Request Wizard__:

   * Enter in the End point for Secret Server.
   * Change the Request Method to __POST__.
   * Change the Accept response as to __JSON__.

1. Click on __Add Parameter__ and add the following parameters shown in the image below.

1. Click on __Add Header__:

   * Enter in __content-type__ for Name.
   * Enter in __application/json__ for Value.

   ![Orchestrator Settings](images/27.png)
1. Click __Preview__.
1. Under the __Response__ tab in the HTTP Request Wizard, you should be able to see the new token.

   ![Orchestrator Settings](images/28.png)
