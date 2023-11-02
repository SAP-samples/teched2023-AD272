


# Risk Management App with SAP Build Apps
<!-- description --> In this exercise, we will create a SAP Build Apps application that calls a CAP Service and will trigger an approval process with SAP Build Process Automation.

## Exercise 1.1 Consume a CAP Service in SAP Build Apps
<!-- description --> Using SAP Build Apps, create an app that calls a CAP service via a destination, updates data, and manages permissions based on SAP BTP role collections.

## Prerequisites
- A CAP service was created and deployed, if you want to try out afterwards you can find a guide here [Create a CAP Service with BAS Productivity Tools](build-apps-cap-service).
- A destination to your CAP service was created, as described in [Expose a CAP Service to SAP Build](build-apps-cap-expose).
- SAP Build Apps on the same tenant to which you deployed your CAP service.


## You will learn
- How to import projects.
- How to create a data resource from a destination.
- How to check BTP permissions to a CAP service.
- How to do CRUD operations in SAP Build Apps for a CAP service.



## Intro
Instead of building the entire project from scratch, you will import a project with all the pages created, all the UI components added to the pages, and all the components stylized. Most bindings will also be set.

The app you will help build has 3 pages:

![App design](/exercises/1_SAPBuildApps/images/appDesign.jpg)

- **Risks:** This page lists all the existing risks (with description and criticality displayed), and includes a button so you can add a new risk.

    Next to each risk is a delete button, which lets you delete a risk from the CAP service.

- **Risk Details:** This page shows all fields for a specific risk, plus the corresponding mitigation selected for the risk (if one exists). The page has 2 actions you can do:

    - There is an **Edit** button to edit the fields. The button takes you to the **Manage Risks** page, which is used for both adding and editing risks.

    - All the existing mitigations are displayed, and you can select one to assign it to the current risk, instead of the currently assigned mitigation.

- **Manage (Add/Update) Risks:** This page lets you add a new risk or update an existing risk (if a risk ID is passed). If you navigate from an existing risk, all the field values for that risk are loaded, and you will be updating that risk.




### Open SAP Build Apps
Open SAP Build Apps with this link: https://ad272-rt8pv9xc.eu10.build.cloud.sap/lobby 

Sign in with tdct3ched1.accounts.ondemand.com.

Login with your user id ad272-XXX@education.cloud.sap where XXX is your assigned user like 001 or 002 and so on and password will be Acce$$teched23

The SAP Build lobby should open.

![Lobby](/exercises/1_SAPBuildApps/images/1-lobby.png)


### Import project

Download the file [Risk ManagementNew.zip.gpg](/exercises/1_SAPBuildApps/images/RiskManagementNew.zip.gpg). Don't use right click, to download it.

![Download](/exercises/1_SAPBuildApps/images/download.jpg)

Create a new SAP Build Apps project from the lobby.
Select Create -> Build an Application -> Web & Mobile Application. Name it Riskmanagement *Your AD272 user id* like **Risk Management AD272-123**

Open your project and then go to the upper-right corner, select the 3 dots and then **Replace** -- this import replaces and deletes the current content of the project.

Select the `zig.gpg` file and click **Replace**.


### Create data resource for CAP app
The first thing you need to do is connect the project to your CAP service via our destination, to retrieve the data. And in order to do this we need to enable SAP BTP authentication.

1. Go to the **Auth tab**.

2. Click **Enable Authentication**, then select **SAP BTP Authentication**.

    ![Enable authentication](/exercises/1_SAPBuildApps/images/3-oauth.jpg)

    Click **OK**.

3. Go to the **Data** tab.

4. Click **Add Integration**.

    ![Add integration](/exercises/1_SAPBuildApps/images/3-add-integration.jpg)

    >Note that there will be many error messages. This is because we already created data variables as well as bindings with those variables, but we deleted the data resources because we wanted you to do that part.

    >You can ignore these error messages. As soon as you create the data resources, they will go away.

5. Click **BTP Destinations**, and then select the destination called **RiskManagement**.

    ![Select destination](/exercises/1_SAPBuildApps/images/3-data-dest.jpg)

6. Click **Install Integration** (upper right).

    ![Alt text](/exercises/1_SAPBuildApps/images/3-data-add-entities.jpg)

7. For each of the two entities, **Risks** and **Mitigations**, click the entity and then click **Enable Data Entity**.

    ![Entities added](/exercises/1_SAPBuildApps/images/3-data-add-entities2.jpg)

You can now click **Browse Real Data** to see live data from the CAP service. After viewing the data, you can close it (X).

![Browse real data](/exercises/1_SAPBuildApps/images/3-data.jpg)

Press **Save**.
In addition, the errors should now be gone. Data variables were already set up on all 3 pages of the app, and now should be functioning properly.


### Risks – Review logic to check permissions
When the first page loads, we want to do 2 things:

- Load the list of risks
- Check whether user has permission to read / write.

Click the **UI Canvas** tab again to go back to the UI, and then open the logic canvas.

![UI canvas](/exercises/1_SAPBuildApps/images/4-UI-canvas.jpg)

You should see the page's main canvas page (the one you get if you click away from any component/variable, that is, in the open gray area). We've added the following logic:

![Initial logic](/exercises/1_SAPBuildApps/images/4-explain-permission-check.jpg)

The logic is triggered when the page opens, and the following is performed:

- **Retrieve Risks:** A call is made to the CAP service to get all the risks.

- **Check Write Permissions:** If reading the CAP service succeeded, we now check if the user has write permission by making an empty update to the first record (the update does not change the record -- PATCH update with no values). If the update fails, we set a page variable to indicate the user does not have write permission.

- **Check Read Permissions:** If reading the CAP service failed, we check if the reason was because of permissions (403 status error). If yes, we set page variables to indicate the user has neither read nor write permissions.

- **Display User Permissions:** After checking permissions, we display a toast message indicating what permission the user has.  

![Display permissions](/exercises/1_SAPBuildApps/images/4-display.jpg)


### Risks – Add logic to navigate to add risk
Now we just want to enable the **Add Risk** button to navigate to the **Manage Risks** page.

- Select the **Add Risk** button and open the logic panel.

  ![Open logic for button](/exercises/1_SAPBuildApps/images/5-open-logic.jpg)

- Add an **Open page** flow function, and connect it to the **Component tab** event. You can connect it it with the little dots next to the components.

  ![Open page](/exercises/1_SAPBuildApps/images/5-add-open-flow.jpg)

- Select the **Open Page** component and set the page to open as **Manage Risks**.

  ![Set page](/exercises/1_SAPBuildApps/images/5-set-page.jpg)

- Click **Save** (upper right).


### Test Application

- Go to the **Launch** tab, then **Open Preview Portal**, then **Web Preview**.

  ![Web preview](/exercises/1_SAPBuildApps/images/6-test-app.jpg)

- Click **Risk Management** to open the app. You should see the first page with a list of risks.

  ![Test risks](/exercises/1_SAPBuildApps/images/6-test-risks.jpg)

- In addition, you see a toast message indicating what permissions you. In this case, since you gave yourself manager permissions, it should say you are a manager.

  ![Permissions](/exercises/1_SAPBuildApps/images/6-permissions-display.png)

- Also, the **Add Risk** button should take you to the **Manage Risks** page (though that page will not let you add a risk yet, and clicking **Create Risk** will not do anything).



- Enter values for the fields (test that priority cannot be more than 5 characters).

- Click **Create Risk**.

  ![Add risk](/exercises/1_SAPBuildApps/images/9-test-app.jpg)

- Now use the navigation menu to return to the main page with all the risks, and make sure your new risk is there.

  ![Navigate back](/exercises/1_SAPBuildApps/images/9-navigate.jpg)

- You should see your new risk.

  ![New risk](/exercises/1_SAPBuildApps/images/9-test-check-back.jpg)

We will check the update functionality later.


### Risk Details – Add logic to edit risk

1. In the upper left, click the link for the **Manage Risks** page.

    ![Next page](/exercises/1_SAPBuildApps/images/9a-open-page.jpg)

    This will take you to the area for managing the app's pages.

2. Click on the **Risk Details** page.

    ![Select page](/exercises/1_SAPBuildApps/images/9a-details-page.jpg)

    >If you don't go to the **Risk Details** page, make sure to save your project (upper right) and try again.

3. Click on the **Edit** button, and open the logic canvas.

    ![Edit logic](/exercises/1_SAPBuildApps/images/9a-edit-button.jpg)

4. Add an **Open page** flow function, and connect it to the **Component tap** event.

    ![Add open page](/exercises/1_SAPBuildApps/images/9a-navigate-page.jpg)

    Configure the **Open page** flow function to open the **Manage Risks** page, and set the **ID** to the **RiskID** page parameter.

    ![Configure open page](/exercises/1_SAPBuildApps/images/9a-configure-open-page.jpg)


### Risk Details – Review logic to change mitigation
We want to enable the user to see all the existing mitigations, and to click on one to make it the mitigation for the current risk.

- Select the list item component (just under the **All Mitigations** text) and open the logic pane.

  ![Initial logic](/exercises/1_SAPBuildApps/images/9b-flow.jpg)

- In this logic flow, we do the following:

  - **Check Need for Update:** We check 2 things to see if we need to do the update at all:

      - Does the user have write permission?

      - Did the user select a different mitigation?

  - **Update Risk:** If both checks are true, we update the risk.

  - **Refresh Risk Details:** We retrieve the risk details in order o refresh the page.

The other flow functions set the **changingMigration** variable in order to display a spinner while we are updating the record.


### Test Application
- Again, go to the **Launch** tab, then **Open Preview Portal**, then **Web Preview**.

- Click **Risk Management** to open the app.

- Click the risk we added earlier.

  ![Display risk](/exercises/1_SAPBuildApps/images/test-1-get-risk.jpg)

- The risk will not have any mitigation. Click one of the mitigations to select it for this risk.

  ![Alt text](/exercises/1_SAPBuildApps/images/test-2a-change-mitigation.jpg)

  ![Alt text](/exercises/1_SAPBuildApps/images/test-2b-change-mitigation.jpg)


## Exercise 1.2 Create a process trigger  
<!-- description --> In this part we will create a form with a submit button that will trigger a process which will be created in the SAP Process Automation part of this exercise.

<br> As a first step we will integrate a data entity from the marketplace, which will be the connection to our approval process.
Select **MARKETPLACE** above the UI components on the left side

![Marketplace](/exercises/1_SAPBuildApps/images/10j-marketplace.jpg)

- Search for the secret key: NorfIxFhC900beCXAAxClA

- Select the data entity **Approval Workflow Trigger** and press **Install** on the top right side.
Press EXIT to close the marketplace.

- Add a new page called **Manage Mitigation**
![Create new page](/exercises/1_SAPBuildApps/images/10a-new-page.jpg)

- Change Headline to **Create new Mitigation**
Afterwards delete the text field and add three input fields.
![Input Fields](/exercises/1_SAPBuildApps/images/10b-mitigation.png)

- Rename the labels to:
  - Owner
  - Timeline
  - Description
  - Afterwards add a button and rename it “Trigger Approval”

    ![Input Fields](/exercises/1_SAPBuildApps/images/10c-approvalbutton.jpg)

- Go to Variables -> Data Variables -> Add a new Data Variable: Approval Workflow Trigger and change the Data Variable type to New data record

  ![Data Variable](/exercises/1_SAPBuildApps/images/10d-data-variable.jpg)

- Open the logic canvas, select the **Set data variable** component and click on "custom object" in the Properties.

- Assign the fields:
 - riskImpact: App Variable: selectedRisk.riskImpact
 - riskCriticality: App Variable: selectedRisk.riskCriticality
 - riskDescription: App Variable: selectedRisk.riskDescription
 - riskResponsible: App Variable: selectedRisk.riskResponsible
 - definitionId: App Variable: definitionId

    ![Fields of Data variable](/exercises/1_SAPBuildApps/images/10i-data-variable.jpg)

- Save and go back to the UI canvas by clicking the **VIEW** toggle

- Map the value of the inputs fields to the approval workflow fields of the data variable **Approval Workflow Trigger1**

  ![Field Mapping](/exercises/1_SAPBuildApps/images/10e-field-mapping.jpg)

- Select the **Trigger Approval** button and open the logic canvas for the button.

- Add a **Create Record**, a **Toast** and an **Alert** and connect it like in the screenshot below:
![Logic Button](/exercises/1_SAPBuildApps/images/10f-logic-button.jpg)

- Modify the Create Record as follow:

 - Recource Name: Approval Workflow Trigger
 - Record: Data Variable **Approval Workflow Trigger1**

 - Change the Toast: -> Toast Message to **Success**
 - Change the Alert: -> Dialog Title to **Error**

Save the application.

- Go to the **Risk Details** page
- Add a new button at the end called **Add new mitigation**

- Add a **open page** logic component and connect it to the "Component tap" event. Set the Page to **Manage Mitigation**.


###### That was it in the SAP Build Apps part.

Now we move over to SAP Build Process Automation:
[Exercise 2 - SAP Build Process Automation](/exercises/2_SAPBuildProcessAutomation/)
