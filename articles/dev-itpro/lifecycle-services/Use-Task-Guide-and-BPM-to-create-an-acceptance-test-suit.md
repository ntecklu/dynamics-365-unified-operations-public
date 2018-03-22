# Use Task Guide and BPM to create an acceptance test suite

You can use Taks Guides and BPM to create your user acceptance test plan. This enables you to organize your acceptance tests by business processes and synchrnoize BPM to VSTS allowing you to manage test execution and results. This article walks through the process of creating an acceptance test suite to be used for either manual or automatic testing in four easy steps.

## 1 .Create a BPM library

There are several ways to create a Business process modeler (BPM) library. For instructions on how to create libraries in BPM see https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/creating-editing-browsing

In this article SHOW USING IMPORT FROM EXCEL 

show example with photos 

**For the purpose of this article describe test case library **

## 2. Record Test Cases and Upload to BPM 

Next you'll need to create your test cases using Task Recorder and upload them to BPM, there are three ways to do this. You can create a new Task Recording and save it to BPM, save an existing Task Reocrding to BPM, or upload an AXTR file to BPM.

### To create a new Task Recording and save to BPM 
First, open the client and log in. Note: It&#39;s good practice to refresh the browser before each new recording. This creates a new user session and restarts Task Recorder, providing the most stable recording experience.

Select the company that you want to use while recording.

Go to **Settings &gt; Task recorder**.

![Select Task Recorder](LINK "Select Task Recorder")

Click **Create a new recording**.

Enter a name for the recording and click **Start**. Recording begins the moment **Start** is clicked.

**Note** : During recording, clicking the &quot; **X**&quot; in the upper-right corner will hide the pane without stopping the recording. The pane can be re-opened by clicking the **Task recorder** menu button that appears at the top of the screen. This icon only appears while recording is in progress

When recording is complete, click **Stop** in the **Task Recorder Pane.**

Click **Save to Lifecycle Services**.

![Task Recorder Option](LINK "Task Recorder Options")

Select the library you want to save the recording to and **Save**.

### To save an existing Task Recording to BPM
IS it just opening up to edit in AX and then saving it ? 


### To upload an AXTR file to BPM 

In Microsoft Dynamics Lifecycle Services (LCS), in your project, on the **Business process libraries** page, select the library to upload the task recording to.

Select the process to upload the task recording to.

In the right pane, select **Upload**. 

![Upload AXTR 1](LINK "Upload AXTR 1")

Select **Browse** to find and select the file to upload, and then select **Upload**.

![Upload AXTR 2](LINK "Upload AXTR 2")


## 3. Sync with VSTS   

To synchronize a BPM library with a VSTS project, you will need to setup a connection between the LCS project and VSTS. For details on how to configure, see [Configure your LCS project and connect to LCS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/synchronize-bpm-vsts#configure-your-lcs-project-to-connect-to-vsts). 

Once configuration is complete, to synchronize a BPM library with a VSTS project, on the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **VSTS sync**.

![VSTS Sync1](LINK "VSTS Sync1")

You can also start VSTS synchronization from the toolbar in a BPM library. Select the ellipsis button (…), and then select **VSTS sync**.

![VSTS Sync2](LINK "VSTS Sync2")


## 4. Create a test suite in VSTS

This guide uses BPM to define a test plan by business processes. For instructions on how to create other test plans, see [Create a test plan and test suite](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/create-a-test-plan).

To create a test suite in VSTS, log into VSTS and select the project you want to test in.

Select **Test** from the toolbar.

Select **+** from the left pane and select **Requirement-based suite**


### Executing manually test cases

For more detailed instructions, see [Run manual tests](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/run-manual-tests).

Log into VSTS and select the project you want to test in

Select **Test** from the toolbar.

Select the test suite you’d like to run from the left pane.

Select **Run** and Microsoft Test Runner will open and run in a new browser. 

Start the app that you want to test. Note: Your app doesn't have to run on the same computer as Test Runner. You just use Test Runner to record which test steps pass or fail while you manually run a test.

Mark each test step as either passed or failed based on the expected results. If a test step fails, you can enter a comment on why it failed.

Select **Create bug** to create a bug to describe what failed.

When you've run all your tests, save the results and close Test Runner. All the test results are stored in VSTS.
You can now see the testing status for the suite and the most recent result for each test. 


### Executing automatic test cases

**ROBERT TO WRTIE**
