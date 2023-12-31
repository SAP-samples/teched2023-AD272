# Configure the SAP Build Process Automation Project

In this exercise, you will configure a SAP Build Process Automation project which can trigger an approval process for the mitigation proposed for the risk in the Risk Managment Build Apps application.

## Pre-requisite
1) SAP Build Process Automation project “Risk and Mitigation Approval Process” is given as a template <br>
2) UI5 Application "customui5.customui5" is already developed, deployed and available to be imported and consumed as an approval form in the process. <br>
   Deevloper tutorials for developing UI5 applications can be found [here](https://community.sap.com/topics/ui5/developing-sapui5-applications) <br>

## Steps to configure the SAP Build Process Automation Project

After completing these steps you will have learnt the following.

1)	How to do a Save as New Project from an existing project
2)	Configure the decision with approver
3)	Import UI5 Form
4)	Add UI5 Form to Process 
5)	Add Action based on CAP Service
6)	Release and Deploy
7)	Test Process

## 1)	How to do a Save as New Project from an existing project
a.	Go to Lobby link https://ad272-rt8pv9xc.eu10.build.cloud.sap/lobby<br>
b. Click on <b>tdct3ched1.accounts.ondemand.com</b><br>
c. Login with your user id ad272-XXX@education.cloud.sap where XXX is your assigned user like 001 or 002 and so on and password will be Acce$$teched23 <br>
d.	Locate the Process Automation type of application with name “Risk and Mitigation Approval Process”<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Locate_Project_1.png)<br>
e.	Click on More options and Choose “Save As New Project”<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Save_New_Project_2.png)<br>

  i.	Choose the option for Select Version as “Editable Version”<br>
  ii.	Give a different project name and description if required<br>
  iii.Click on “Save as new”<br>
  <br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Save_As_New_3.png)<br>

  A new project is created now<br>
  
## 2)	Configure the decision with approver

a.	Click on Decision “Determine Risk and Mitigation Approvers”<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Decisions_Click_4.png)<br>
b.	Click on “Rules” and “Approver Determination Rule” <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Rule_Click_5.png)<br>
c.	Change the “Risk Description”, “Risk Criticality”, “Risk Impact” to whatever risk you had created in Build Apps application <br>
d.	Change the “Approver Name” and “Approver Email” to your user’s name and email <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Decision_Edit_6.png)<br>
e.	Save it <br>

Decision is configured to return the approver now <br>

## 3)	Import UI5 Form

a.	Click on Overview section<br>
b.	Click on Import->Form <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Import_Form_7.png)<br>
c.	Enter the Application ID as “customui5.customui5” <br>
d.	Enter the Application Version as 1.0.2 <br>
e.	Enter the name as “Risk and Mitigation UI5 Approval Form XXX”  replace XXX with your ID<br>
f.	Enter the description as “A UI5 form for approval of risks and mitigations” <br>
g.	Click on Import <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/UI5_Form_8.png)<br>
h.	You should get a “Imported” message <br>

UI5 Form is imported to process now <br>

## 4) Add UI5 Form to Process 
  a.Click on the process Risk and Mitigation Approval Process under Artifacts in the Overview 	
   <br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Process.jpg)<br>
  b.Click on the existing “Risk and Mitigation Approval Form” <br>
  c.	Click on the 3 dots and Remove <br>
  <br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Form_removal_9.png)<br>
  d.	Click on + next to Decisions <br>
  e.	Choose Approvals - > Risk and Mitigation UI5 Approval Form XXX<br>
  <br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Add_UI5_Form_10.png)<br>
  f.	Connect the + next to Reject to the Rejection Notification Mail step <br>
  g.	In the General tab, Subject field needs to be filled up . Add the Subject as “Mitigation approval form for” and choose from the Process Inputs, the “MitigationDescription” field <br>
  h.	In the General tab, Users field needs to be filled up. Add the User from Determine Approvers->Approver Email field <br>
  <br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Fill_Mandatory_Details_UI5_11.png)<br>
  i.	In the Inputs field, map the fields in UI form to the Process Inputs for the actual values to be populated in the form <br>
        i.	Migration Description <br>
        ii.	Migration Owner <br>
        iii.Migration Timeline <br>
        iv.	Risk Criticality <br>
        v.	Risk Description <br>
        vi.	Risk Impact <br>
        vii.	Risk Responsible <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Mapping_UI_Fields_12.png)<br> 
i.	  Save the form <br>

Now the UI5 form is added as the approval form now.

## 5)	Add Action based on CAP Service
An Action project based on CAP Service which helps to create a single mitigation on approval of the process is already created  and deployed onto the tenant.
This action can be consumed in the process now <br>

Please refer to the following links for know hows on CAP Service creation and consumption. Please note that these are already done and you don't have to do these as part of this exercise<br>

1.[Create a CAP Service with BAS Productivity Tools](https://developers.sap.com/tutorials/build-apps-cap-service.html) <br>
2.[Create a destination to your CAP service](https://developers.sap.com/tutorials/build-apps-cap-expose.html) <br>
3.[Create Action Project for CAP Service](https://developers.sap.com/tutorials/spa-consume-actions-cap-action-create.html) <br>

a.	Click on the + next to Approve in the Approval form <br>
b.	Choose Actions->Browse Library <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Add_Actions_13.png)<br> 
c.	Choose “Create a Single Mitigation” from project Risk Management Actions and Add <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Action_Choose_Library_14.png)<br> 
d.	In the General tab, fill the destination variable with “CAPService” <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Actions_Inputs_Fill_15.png)<br> 
e. In the General tab, fill the "Run step on behalf of" with the Process Started By attribute from Process Metadata . This is needed to do principal propogation during the call to Action based on CAP Service<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Run_Onbehalf.jpg)<br> 
f.	In the Inputs section, <br>
  i.	Fill the description field with “Mitigation Description” from Process Inputs <br>
  ii.	Fill the owner field with “Mitigation Owner” from Process Inputs <br>
  iii.	Fill the timeline field with “Mitigation Timeline” from Process Inputs <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Action_Input_Fill_16.png)<br> 
g.	Save it <br>

Now the Action based on CAP Service is added which will post the mitigation to SAP HANA <br>

## 6)	Release and Deploy

The destination “RiskManagement_OAUTH” is already created in BTP cockpit and added in settings for you to use it directly<br>
Please refer to the following link to know on 
[How to Create Destination in the SAP BTP Cockpit](https://developers.sap.com/tutorials/cp-cf-create-destination.html)<br>
The created destination is then added to the Settings to use it in the project <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Destination_Settings.png)<br>
a.	In the Overview page of the project, Click on Release button <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Release_Project_17.png)<br> 
b.	Give a Version Number , for example, 1.0.1 <br>
c.	Give a Version Comment, for example, “Initial Draft” <br>
d.	Click on Release <br>
e.	In the Overview page of the project, now you can see a Deploy button(if the previous step of Release was successful) <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Deploy_Project_!8.png)<br> 
f.	Click on Deploy button , say Next <br>
g.	Choose the destination as “RiskManagement_OAUTH” and say Next. <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Deploy_Project_!9.png)<br> 
h.	Click on Deploy button <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Deploy_Project_20.png)<br> 
i.	In case of successful deployment, “Risk and Mitigation Approval Process has been deployed” message will pop up. <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Deploy_Project_21.png)<br> 
j. Go to Monitoring - > Process and Workflow Defintions and search for your project <br>
k. Check mark your project and select it .<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Search_project.jpg)<br> 
j. You can find the ID which is the definition id of the process, note it and keep it ready for the next exercise.<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Def_Id.jpg)<br> 




## Summary

Now that you have configured , released and deployed the SAP Build Process Automation project, Continue to - [SAP Build Apps Deployment](/exercises/2_BuildAppsDeploy/README.md)
