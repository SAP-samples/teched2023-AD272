# Configure the SAP Build Process Automation Project

In this exercise, you will configure a SAP Build Process Automation project which can trigger an approval process for the mitigation proposed for the risk in the Risk Managment Build Apps application.

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
b.	Locate the Process Automation type of application with name “Risk and Mitigation Approval Process”<br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/Locate_Project_1.png)<br>
c.	Click on More options and Choose “Save As New Project”<br>
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
e.	Enter the name as “Risk and Mitigation UI5 Approval Form” <br>
f.	Enter the description as “A UI5 form for approval of risks and mitigations” <br>
g.	Click on Import <br>
<br>![Process design](/exercises/2_SAPBuildProcessAutomation/images/UI5_Form_8.png)<br>
h.	You should get a “Imported” message <br>

UI5 Form is imported to process now <br>

## 4) Add UI5 Form to Process 

## 5)	Add Action based on CAP Service

## 6)	Release and Deploy

## 7)	Test Process

## Summary

Now that you have configured and tested the SAP Build Process Automation project, Continue to - [SAP Workzone configuration](/exercises/3_SAPBuildWorkZone/README.md)
