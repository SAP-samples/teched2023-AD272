
# Create and design a Site Using SAP Build Work Zone, standard edition
<!-- description --> Using SAP Build Work Zone, create a business site to create, view and handle risks. 

 
## Prerequisites
- A CAP service was created and deployed, if you want to try out afterwards you can find a guide here [Create a CAP Service with BAS Productivity Tools](build-apps-cap-service).
- A destination to your CAP service was created, as described in [Expose a CAP Service to SAP Build](build-apps-cap-expose).
- You created an app using SAP Build Apps on the same tenant to which the CAP service is deployed.
- You integrated your process to your App.
- You have subscribed to SAP Build Work Zone, standard edition and was assigned to the Launchpad_Admin role.



## You will learn
- How to create a site using SAP Build Work Zone, standard edition
- How to design a site with the new experience and create a custom Space and Page
- How to integrate your app to your site
- How to integrate pre-deployed UI integration cards to your site 



## Intro
In this tutorial you will create and design your own business site using SAP Build Work Zone, standard edition. You will integrate to your site the app you developed using SAP Build Apps, and UI integration cards that are already deployed to the subaccout.

The site you will design will have a Space and a page:

![App design](appDesign.jpg)



### Open SAP Build Work Zone, standard edition
Open SAP Build Work Zone, standard edition,  with this link:  [SAP Build Work Zone, standard edition](https://ad272-rt8pv9xc.dt.launchpad.cfapps.eu10.hana.ondemand.com/sites#Site-Directory).

The SAP Build lobby should open.

![Lobby](1-lobby.png)





- **Risks:** This page lists all the existing risks (with description and criticality displayed), and includes a button so you can add a new risk.

    Next to each risk is a delete button, which lets you delete a risk from the CAP service.

- **Risk Details:** This page shows all fields for a specific risk, plus the corresponding mitigation selected for the risk (if one exists). The page has 2 actions you can do:

    - There is an **Edit** button to edit the fields. The button takes you to the **Manage Risks** page, which is used for both adding and editing risks.

    - All the existing mitigations are displayed, and you can select one to assign it to the current risk, instead of the currently assigned mitigation.

- **Manage (Add/Update) Risks:** This page lets you add a new risk or update an existing risk (if a risk ID is passed). If you navigate from an existing risk, all the field values for that risk are loaded, and you will be updating that risk.
