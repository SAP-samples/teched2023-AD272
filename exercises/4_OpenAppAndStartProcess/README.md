# Exercise 4 - Open your site runtime, launch the Risk Management Application and Start Process

In this exercise, we will create connect all the SAP Build artificats and run the application, and experience it from an end user perspective. 

## Exercise 4.1 Open your site in runtime

1. In SAP Build Work Zone site directory, click the arrow icon next to your site to navigate to your site runtime

![Work Zone](/exercises/4_OpenAppAndStartProcess/Images/Go-to-site-1.png)
This is the site the end users will access as a central entry point to handle Risks

2. You can now view the site, cards and apps of this site. The card below shows you all the risks in a visual way that helps users be aware of the risks in a visual way.

To handle risks, launch your app for Risk Management and click on your app tile 
![Work Zone](/exercises/4_OpenAppAndStartProcess/Images/Go-to-site-2.png)


## Exercise 4.2 Open your app and add a new mitigation
1. Select the risk that you have created.

![Open Risk](/exercises/4_OpenAppAndStartProcess/Images/sba-run1.jpg)

2. Scroll down to the button of the mitigations and press the button **Add new mitigation**

![Add new mitigation](/exercises/4_OpenAppAndStartProcess/Images/sba-run2.jpg)
3. Enter some data that you can identify easily and press the **Trigger Approval** button. Now your own approval workflow is started.

![Open Risk](/exercises/4_OpenAppAndStartProcess/Images/sba-run3.jpg)

After the approval you can come back to the app and you should see your new mitigation and assign it to the risk.

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
7.	Go to My Inbox to approve the task  <br>
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/MyInbox_WZ.png)<br>
8.	In the My Inbox application, the approval form can be seen with Risk Information, Mitigation Information and Comments section along with Approve/Reject buttons <br>
   <br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_4.png)<br>
   <br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Monitor_process_5.png)<br>
9.	You can provide a comment and Approve or Reject the Risk and Mitigation request <br>
10.	If you have approved , there will be a CAP Service call via action which posts the mitigation details to the HANA DB <br>
11. You should be able to see it in the Monitor process that the creation of single mitigation is successful <br>
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Mitigation_Creation_Success.png)<br>
12.	This can be verified in the Build Apps application.You should be able to see this new mitigation which you can assign to the risk <br>
<br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Mitigation_Creation_Success_BA.png)<br>
13.	There will be a mail notification which is triggered to the user who started the process with the risk and mitigation description along with the comments <br>
 <br>![Process design](/exercises/4_OpenAppAndStartProcess/Images/Mail.png)<br>
14.	If you have rejected, there is a  mail notification which is triggered to the user who started the process with the comments provided by the approver <br>

   
## Summary

You've now leaent how to open , start and monitor a process with SAP Build Apps, SAP Build Process Automation and SAP Build Workzone.


