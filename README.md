## Table of contents

- [Automation Process Overview](#automation-process-overview)
- [Stretch Tasks](#stretch-tasks) 
- [How to use the Process](#how-to-use-the-process) 
- [References](#references) 

## Automation Process Overview
The UiPath User Acceptance Testing automation process has some of the following core features:
- It tests CRUD operations.
- It first adds all the records for a selected entity (e.g., Customer), then edits all records, and then deletes all records.
- The user can select which entities to test during a run.
- The automation process logs the user in at the start of a run, and logs the user out at the end of the run.

## Stretch Tasks
After a run, if there was a record that failed, the output in the test data file would only indicated that a record has failed and not provide any additional information regarding at which step it failed (e.g., creating, editing, deleting).\
It was decided that as a strecth goal, to add the functionality to provide this information in the test data file.  At each step, if a record does fail, an entry is made that indicates at which step it failed.  That record is will then no further be manipulated by any additional steps, as to remain in the state that it was in at the point of failure.  That way the user can inspect what the record looked like when it failed, and perhaps better ascertain the cause of the failure.

## How to use the Process
When the process is started, the user will be asked input in a series of seven step.  These steps will determine as what account to log in as, which test data file to use, as well as which tests to run.\

**Two very important things to remember when using the process is:**
- Always ensure that you are logged out of the web application before running the process.
- Make sure to not have the web application open in any browsers/tabs before/while running the process.

**Process Startup Steps:**
- Step 1
    - Provide the user email address of the account that will be used to log into the web application that is tested.

- Step 2
    - Provide the password used to log in the provided account.

- Step 3
    - Select the xlsx file that contains the test data.  This file will also be used to provide the output.  The directory of file can be pathed to with the input box.

- Step 4
   - Select whether to test for Customers.

- Step 5
   - Select whether to test for Products.

- Step 6
   - Select whether to test for Orders.

- Step 7
   - Select whether to test for OrderDetails.

## References
https://docs.uipath.com/studio/standalone/2023.4/user-guide/ui-automation. (Accessed: 27 September 2023).

https://www.uipath.com/learning/video-tutorials/excel-datatables-automation. (Accessed: 27 September 2023).

https://www.youtube.com/watch?v=A8cLOfItmv8. (Accessed: 28 September 2023).

https://www.youtube.com/playlist?list=PLhTE7-JU1rhapvY5Z8d22Zun_IRTa6IG2. (Accessed: 28 September 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/install-studio. (Accessed: 28 September 2023).

https://www.mindluster.com/lesson/99261. (Accessed: 02 October 2023).

https://academy.uipath.com/courses/meet-the-uipath-platform. (Accessed: 03 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/introduction. (Accessed: 03 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/about-automation-projects. (Accessed: 03 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/workflow-design. (Accessed: 03 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/sequences. (Accessed: 03 October 2023).

https://academy.uipath.com/courses/build-your-first-process-v202110. (Accessed: 04 October 2023).

https://academy.uipath.com/courses/a-day-in-the-life-of-an-rpa-developer-. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/about-selectors. (Accessed: 04 October 2023).

https://docs.uipath.com/activities/other/latest/ui-automation/advanced-descriptor-configuration. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/control-flow-activities. (Accessed: 04 October 2023).

https://docs.uipath.com/activities/other/latest/productivity/outlook-application-card. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/about-publishing-automation-projects. (Accessed: 04 October 2023).

https://docs.uipath.com/robot/standalone/2021.10/user-guide/about-uipath-assistant. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/the-user-interface. (Accessed: 04 October 2023).

https://docs.uipath.com/process-mining/automation-cloud/latest/user-guide/introduction-to-process-mining. (Accessed: 04 October 2023).

https://www.uipath.com/blog/product-and-updates/accelerating-automation-development. (Accessed: 04 October 2023).

https://www.uipath.com/blog/automation/simple-framework-determining-what-to-automate. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/automation-lifecycle. (Accessed: 04 October 2023).

https://www.uipath.com/rpa/robotic-process-automation. (Accessed: 04 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/managing-variables. (Accessed: 05 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/flowcharts. (Accessed: 06 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/state-machines. (Accessed: 06 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/global-exception-handler. (Accessed: 06 October 2023).

https://docs.uipath.com/activities/other/latest/workflow/invoke-workflow-file. (Accessed: 06 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/managing-arguments. (Accessed: 06 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/using-arguments. (Accessed: 06 October 2023).

https://academy.uipath.com/courses/variables-and-arguments-in-studiov202110. (Accessed: 09 October 2023).

https://docs.uipath.com/studio/standalone/2021.10/user-guide/example-of-using-an-array-variable. (Accessed: 09 October 2023).

https://docs.uipath.com/studio/standalone/2023.4/user-guide/uipath-explorer. (Accessed: 11 October 2023).

https://www.youtube.com/playlist?list=PLEYSwx3duQ2DduxR5-9rZgE7glvhoLYjO. (Accessed: 12 October 2023).

https://www.youtube.com/watch?v=fBMoaoOoxfI. (Accessed: 12 October 2023).

https://www.youtube.com/playlist?list=PLgY1FEm82KyVl9aHmRMo6EQQjDA3P0dMt. (Accessed: 12 October 2023).

https://docs.uipath.com/activities/other/latest/workflow/input-dialog. (Accessed: 12 October 2023).

https://docs.uipath.com/activities/other/latest/productivity/excel-process-scope-x. (Accessed: 13 October 2023).

https://www.youtube.com/watch?v=wk2PBLU3mg0. (Accessed: 13 October 2023).

https://www.youtube.com/watch?v=8V_DhzPsuAo. (Accessed: 14 October 2023).

https://www.youtube.com/watch?v=yKtRJJZz8OM. (Accessed: 16 October 2023).

https://www.youtube.com/watch?v=txVPbzRoXsg. (Accessed: 16 October 2023).

https://www.youtube.com/watch?v=gkmjZusQyqk. (Accessed: 16 October 2023).

https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180. (Accessed: 18 October 2023).