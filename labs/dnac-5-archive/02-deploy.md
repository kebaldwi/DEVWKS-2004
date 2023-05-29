# Archiving Device Configurations

We will now use the REST-API's within the collection `Configuration Archive` to pull the configuration archives for all devices within the inventory. 

This collection will first get a list of devices, then download the configuration archive for each one. You will need to save the responses to download them.

Follow these steps:

1. Navigate and open the desired collection runner through the following:

   1. Within Postman, click on the collection shortcut in the sidebar
   2. Hover over the collection `DNA Center API LAB 304 - Configuration Archive`
   3. Click the `Run Collection` submenu option

      ![json](./images/Postman-Collection-ConfigArchive.png?raw=true "Import JSON")

2. To run the collection, do the following:

   1. Locate the sub-components of the `Runner`
   2. Optionally select the `Save Responses` option
   3. Click  the `Run DNA Center API LAB 304 - Configuration Archive` button

      ![json](./images/Postman-Collection-ConfigArchive-Runner.png?raw=true "Import JSON")

3. The following summary will slowly appear as the collection is processed

   1. Copy the Password `TestT3$t` to open the zip file later.
 
      ![json](./images/Postman-Collection-ConfigArchive-Summary.png?raw=true "Import JSON")
 
   2. Click the console at the bottom of Postman and search for the last API call made.

      ![json](./images/Postman-Collection-ConfigArchive-Console.png?raw=true "Import JSON")

   3. Expand the results of the API call and open the `Response Body`
   4. Notice the file response does have the Configurations in it. This API Collection collected all of them and, if exported to a Python system, could save them to a local file folder.

      ![json](./images/Postman-Collection-ConfigArchive-Console-Results.png?raw=true "Import JSON")

4. Click on the collection `DNA Center API LAB 304 - Configuration Archive` to expand it in the left pane, then do the following:

   1. Click on the Rest-API `Get Results` sub-component to open it on the right
   2. Click on the little arrow on the right of `Send` to expose a submenu
   3. Click `Send and Download` to send this Rest-API and automatically download what is retrieved

      ![json](./images/Postman-Collection-ConfigArchive-ResultsAPI.png?raw=true "Import JSON")

5. As the Rest-API `Get Results`completes an explorer window will prompt to save the results to the desktop click ok to save the file

   ![json](./images/Postman-Collection-ConfigArchive-ResultsAPI-Send.png?raw=true "Import JSON")

6. Locate the zip file on the desktop, and extract it using whatever extraction tool is available to your system. WinRar is what can be used and is displayed here.

   ![json](./images/Postman-Collection-ConfigArchive-Extract.png?raw=true "Import JSON")

7. During Extraction, you will be prompted for the password we stored from step 6, but again it is `TestT3$t` in the event you can't locate it. Enter the password as prompted and complete the extraction.

   ![json](./images/Postman-Collection-ConfigArchive-Pwd.png?raw=true "Import JSON")

8. Locate the Extracted folder and open one of the text-based files within to reveal the configuration selected.

   ![json](./images/Postman-Collection-ConfigArchive-Verify.png?raw=true "Import JSON")

> [**Next Section**](./dnac-5-archive/03-summary.md)