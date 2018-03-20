# Use Task Guide and BPM to create an acceptance test suite

You may now use Taks Guides and BPM to represent your user acceptance test plan and help you organize your acceptance tests by business processes. This article walks through the process of creating an acceptance test suite to be used for either manual or automatic testing in four easy steps.

## 1 .Create a BPM library

There are two ways to create a Business process modeler (BPM) library. You can create a new library that has no lines or task recordings, or you can copy an existing library.

In Microsoft Dynamics Lifecycle Services (LCS), open a project, click on the **More tools** dropdown, and then click **Business process modeler**.

![Navigate To BPM](LINK "Navigate To BPM")

To create a new library, right-click any library, and then, in the lower-left corner of the window, click *![alt text]("")*Create**.

![Create New Library](LINK"Create New Library")

Or, to copy an existing library, right-click that library, and then, in the lower-left corner of the window click, **Copy.**

![Copy Library](LINK"Copy Library")

Then Enter a name for the library and click **Create**.

## 2. Create and Save or Upload Task Recording to BPM

Next you'll need to connect a Task Recording to BPM, there are three ways to do this. You can create a new Task Reocrding and save it to BPM, 
save an existing Task Reocrding to BPM, or upload an AXTR file to BPM.

### To create a new Task Recording and save to BPM 
First, open the client and log in. Note: It&#39;s good practice to refresh the browser before each new recording. This creates a new user session and restarts Task Recorder, providing the most stable recording experience.

Select the company that you want to use while recording.

Go to **Settings &gt; Task recorder**.

Click **Create a new recording**.

Enter a name for the recording and click **Start**. Recording begins the moment **Start** is clicked.

**Note** : During recording, clicking the &quot; **X**&quot; in the upper-right corner will hide the pane without stopping the recording. The pane can be re-opened by clicking the **Task recorder** menu button that appears at the top of the screen. This icon only appears while recording is in progress

When recording is complete, click **Stop** in the **Task Recorder Pane.**

Click **Save to Lifecycle Services**.

Select the library you want to save the recording to and **Save**.

### To save an existing Task Recording to BPM
?????????????????



### To upload an AXTR file to BPM 

In Microsoft Dynamics Lifecycle Services (LCS), in your project, on the **Business process libraries** page, select the library to upload the task recording to.

Select the process to upload the task recording to.

In the right pane, select **Upload**. 

Select **Browse** to find and select the file to upload, and then select **Upload**.


## 3. Sync with VSTS   

To synchronize a BPM library with a VSTS project, you will need to setup a connection between the LCS project and VSTS. For details on how to configure, see [Configure your LCS project and connect to LCS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/synchronize-bpm-vsts#configure-your-lcs-project-to-connect-to-vsts). 

Once configuration is complete, to synchronize a BPM library with a VSTS project, on the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **VSTS sync**. 


## 4. Create a test suite in VSTS

To run manual or automatic testing, you will need to first create a test plan. For detailed instructions, see [Create a test plan and test suite](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/create-a-test-plan). 


### Executing manually test cases

For more detailed instructions, see [Run manual tests](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/run-manual-tests).

### Executing automatic test cases

For more detailed instructions, see [Setup continuous testing](https://docs.microsoft.com/en-us/vsts/build-release/test/set-up-continuous-testing-builds)
