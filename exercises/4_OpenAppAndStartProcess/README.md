# Exercise 4 - Open your site runtime, launch the Risk Management Application and Start Process

In this exercise, we will create connect all the SAP Build artificats and run the application.

## Exercise 4.1 Open your site in runtime
In SAP Build Work Zone site directory, click the arrow icon next to your site to navigate to your site runtime

![Work Zone](/exercises/3_SAPBuildWorkZone/images/Go-to-site-1.png)



## Monitor process in SAP Build Process Automation

After completing these steps you will have learnt on how you can monitor a running process in SAP Build Process Automation

1.	Go to https://ad272-rt8pv9xc.eu10.build.cloud.sap/monitor/dashboard <br>
2.	Go to Manage->Processes and Workflows <br>
3.	Search for project "Risk and Mitigation Approval Process" and choose it <br>
4.	Click on Show Instances <br>
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_1.png)<br>
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_2.png)<br>
5.	You can see the running process
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_3.png)<br>
6.	You can see that there is a task available for approval from the logs of the running process <br>
7.	Go to My Inbox to approve the task (TBD - To upload an image once Iris configures My Inbox in WZ) <br>
8.	In the My Inbox application, the approval form can be seen with Risk Information, Mitigation Information and Comments section along with Approve/Reject buttons <br>
   <br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_4.png)<br>
   <br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_5.png)<br>
9.	You can provide a comment and Approve or Reject the Risk and Mitigation request <br>
10.	If you have approved , there will be a CAP Service call via action which posts the mitigation details to the HANA DB <br>
11.	This can be verified in the Build Apps application (TBD- Sync with Marc for the image to be uploaded) <br>
12.	There will be a mail notification which is triggered to the user who started the process with the risk and mitigation description along with the comments <br>
13.	If you have rejected, there is a  mail notification which is triggered to the user who started the process with the comments provided by the approver <br>

   
## Summary

You've now leaent how to open , start and monitor a process with SAP Build Apps, SAP Build Process Automation and SAP Build Workzone.


