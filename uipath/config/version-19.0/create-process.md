[title]: # (Create a Process and Schedule in UiPath Orchestrator)
[tags]: # (configuration)
[priority]: # (307)
[display]: # (none)
# Create a Process and Schedule in UiPath Orchestrator
<!-- add troubleshooting topic and info -->

## Create a Process

   >**Note:** The example below shows how to create a process that will copy the content from a website and paste it into notepad. The process can be modified or changed to complete other tasks depending on what the user is trying to accomplish.

1. Navigate to __UiPath studio console__.

   ![Tag](images/config35.png)
1. Click __Process__.

   ![Tag](images/config36.png)
1. Name the new Process and click __Create__.

   ![Tag](images/config37.png)
1. Click on the __Project__ tab.
1. Click on __New | Sequence__.

   ![Tag](images/config38.png)
1. Name the new Sequence and click __Create__.

   ![Tag](images/config39.png)
1. Click on the __(+)__ icon under Drop Activity Here.

   ![Tag](images/config44.png)
1. In the search area, enter in __Open Browser__.

   ![Tag](images/config45.png)
1. Click on __Open Browser__.

1. Under the option for Insert URI here, copy and paste in the web based URL from the browser. Example, https://wwww.uipath.com/product/studio.

   ![Tag](images/config46.png)
1. Click on __Save__.

   ![Tag](images/config47.png)
1. Under the __Do__ section of the sequence, click on the __(+)__ icon.

   ![Tag](images/config48.png)
1. In the search area, enter in __Get Visible Text__.
1. Click on Get __Visible Text__.

   ![Tag](images/config49.png)
1. Click on __Indicate element inside the browser__.

   ![Tag](images/config50.png)
1. Select the text in the browser, you would like to copy into the text file.

   ![Tag](images/config51.png)
1. In UiPath Studio console, select the top level on the sequence.

   ![Tag](images/config52.png)
1. Click on __Create Variable__.

   ![Tag](images/config53.png)
1. Enter in __GetText__, under Name.

   ![Tag](images/config54.png)
1. Click on the __Get Visible Text 'H1'__ header.

   ![Tag](images/config55.png)
1. On the right side of the screen, under Properties and Output, click on Text.
1. Enter in __GetText__.

   ![Tag](images/config56.png)
1. Click on the __(+)__ icon for Add activity.

   ![Tag](images/config57.png)
1. In the search area, enter __Open Application__.
1. Click on __Open Application__.

   ![Tag](images/config58.png)
1. Open __Notepad__.
1. Click on __Indicate window on screen__.

   ![Tag](images/config59.png)
1. Outline the Notepad window.

   ![Tag](images/config60.png)

   >**Note:**The filename path under properties on the right-hand side of the screen should show `C:\Windows\System32\notepad.exe`.

   ![Tag](images/config61.png)
1. To copy the text we previously selected from the web browser, into NotePad once the process runs. Click on __(+)__ icon for __Add Activity__.

   ![Tag](images/config62.png)
1. In the search area, enter __Type Into__.
1. Click on __Type Into__.

   ![Tag](images/config63.png)
1. Click on __Indicate element inside the window__.

   ![Tag](images/config64.png)
1. Crop the area inside of the Notepad window, where the text should appear.

   ![Tag](images/config65.png)
1. Click on the __Text must be Quoted__ area.
1. Type in __GetText__.

   ![Tag](images/config66.png)
1. Click __Save__ at the top of the screen.

   >**Note:** If you would like to confirm the process has been completed successfully,  click __Analyze file |  Validate File__. There should be zero errors listed if the process is properly completed.

   ![Tag](images/config67.png)

   ![Tag](images/config68.png)

1. To complete the process, click on Publish.

   ![Tag](images/config69.png)
1. Ensure that the radio button for Orchestrator is select.
1. Click Publish.

   ![Tag](images/config70.png)

   ![Tag](images/config71.png)
1. You can view the published process under Packages in the browser for UiPath Orchestrator.

   ![Tag](images/config72.png)

## Create a new schedule for the process

1. Create a new schedule for the process by navigating to __Triggers__.
1. Click the __(+)__ plus icon.

   ![Tag](images/config73.png)
1. Enter in the following information for the trigger:
   * __Process name:__ Enter in a name for the trigger
   * __Process:__  select from the drop-down "New Process name"
   * __Execution Target:__ Previously configured robot
   * __Trigger interval:__ Starting at every 1 minute, but you can change to a desired time.

   ![Tag](images/config74.png)
1. Click __Save__.
1. Click the __More Actions__ icon.
1. Click __Enable__.

   ![Tag](images/config75.png)
