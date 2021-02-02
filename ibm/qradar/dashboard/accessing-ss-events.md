[title]: # (Accessing Secret Server Events)
[tags]: # (events)
[priority]: # (302)
# Accessing Secret Server Events in the Secret Server Application within QRadar

1. Login to qradar to QRadar as the admin user: `https://<ipaddress>`

   ![](images/8a69f0826c6758514ab82ae604b22048.png)

1. Click on Log activity, select the log from Secret server, then click on DSM
    editor under admin. (Required configuration for application integration)

   ![](images/6afd2274a6fdf25edd152ceec32594f9.png)

1. Select the log Source popup will be displayed, create new or select the
    existing one. (Required configuration for application integration).

   ![](images/0ac8a336f2bef3f5b5f4aea1f44fb808.png)

1. Click on Event Mapping category and click on Add option to map the event
    with event ID. In the DSM editor you need values showing up in the Log
    Preview for both __"Event ID"__ and __"Event Category".__  (NOT REQUIRED FOR APPLICATION INTEGRATION).

   ![](images/acc3fb737045ee63d962ad29bd26e324.png)

## How to create a new QID (OPTIONAL)

1. Click on the button Choose QID

   ![](images/49d8aaf2e76569e35e4be00941dc7c4b.png)

1. Click on Create New QID Record button or select the existing one.

   ![](images/cd59576f731cb4d288757eaf32d023e4.png)

1. (OPTIONAL) Click on add a new Event Mapping using the same two values for Event ID and Category. The last step is to choose the event. Either selects an existing event name by searching using the search field, or create a new record ("Create New QID Record"). The Event ID, Event Category that is used to match the Event depend on using the same value.  

For more info click on : <https://developer.ibm.com/qradar/develop-dsm/>

## Add Custom Properties in __Log Source__

1. Click on __Properties__ tab and click on __+ icon__ to add new properties.

   ![](images/6d79b09dd0adbcb90220a03c1ef2fda8.png)

1. Click on __Create New__ button to add New Properties __ItemId__ and __Item Name__.

   ![](images/c7fd8bf2e0d5288d5dc350ae637a437f.png)

## Create Custom Property

1. Create two properties __ItemId__ and __Item Name__.
1. Check the check box to __enable the properties in Rules and Search indexing__ before clicking on the __Save__ button.

   ![](images/03ed0433a78ceda2f53c8c29770c3f7f.png)

After properties have been added they will be displayed under __Properties tab__ in the selected __log source type__.

   ![](images/7bda78c203555a58d9e0c241bad23a6f.png)

## Enable access to property values

1. Click on created properties

1. Enter the following expression

   * Field Name: __Item Id__       expression: __Item Id__:\s(\d*)

   * Field Name: __Item Name__     expression: __(?<=Item Name: ).+?(?=\(Item Id)__  

   ![](images/91297c0ddc9778e2af5fc13098a3a71c.png)

1. click on __Ok__.

## Enable Configuration

1. Click on __Configuration__ option.

1. __Enable__ the __Log property Auto Detection__ option.

1. __Enable Properties for use in Rules and Search indexing__.

   ![](images/c7c21402800cf4a47f411bd55fa5cd64.png)

1. Select __CEF__ from the dropdown in __Property Detection Format__.

   ![](images/465a51d52902899d858ecacd34e14a4c.png)

1. __Click Save__.

## Create log source

1. Click __on Admin | Log source__.

   ![](images/07cf3a6e0a06e6c52dd562302b247ab5.png)

1. Click on the __Add__ button.

1. Add log source popup will be displayed.

   * Enter the Name

   * Description

   * Select the log source type created in above steps.

   * Enter the __Log source Identifier__ as Host Name of machine where Secret Server is installed.

1. Click __Save__.

   ![](images/54f2261433114e0f3fabd1420e089ba0.png)

## Deploy Log Source

1. On the Admin Page of QRadar, click on __deploy changes__ button.

   ![](images/48c6869e6d9f8a58aacabfaa0e936afb.png)

## (OPTIONAL) Validate Log Source

1. Click on __Log Activity__ | __add filter__.

1. Select the log source.

   ![](images/e03d1466d6a02844923edad90c32acf1.png)

1. We would be able to see the log under log source which we have created using DSM editor

   ![](images/7da125d55b02ed9f5e578fa781bcad3c.png)
