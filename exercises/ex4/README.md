
# Consume a CAP Service in SAP Build Apps
<!-- description --> Using SAP Build Apps, create an app that calls a CAP service via a destination, updates data, and manages permissions based on SAP BTP role collections.

 
## Prerequisites
- A CAP service was created and deployed, if you want to try out afterwards you can find a guide here [Create a CAP Service with BAS Productivity Tools](build-apps-cap-service).
- A destination to your CAP service was created, as described in [Expose a CAP Service to SAP Build](build-apps-cap-expose).
- SAP Build Apps on the same tenant to which you deployed your CAP service.



## You will learn
- How to import projects
- How to create a data resource from a destination
- How to check BTP permissions to a CAP service
- How to do CRUD operations in SAP Build Apps for a CAP service  



## Intro
Instead of building the entire project from scratch, you will import a project with all the pages created, all the UI components added to the pages, and all the components stylized. Most bindings will also be set.

The app you will help build has 3 pages:

![App design](appDesign.jpg)

- **Risks:** This page lists all the existing risks (with description and criticality displayed), and includes a button so you can add a new risk.

    Next to each risk is a delete button, which lets you delete a risk from the CAP service.

- **Risk Details:** This page shows all fields for a specific risk, plus the corresponding mitigation selected for the risk (if one exists). The page has 2 actions you can do:

    - There is an **Edit** button to edit the fields. The button takes you to the **Manage Risks** page, which is used for both adding and editing risks.

    - All the existing mitigations are displayed, and you can select one to assign it to the current risk, instead of the currently assigned mitigation.

- **Manage (Add/Update) Risks:** This page lets you add a new risk or update an existing risk (if a risk ID is passed). If you navigate from an existing risk, all the field values for that risk are loaded, and you will be updating that risk.




### Open SAP Build Apps
Open SAP Build Apps with this link: "missing link to lobby"

The SAP Build lobby should open.

![Lobby](1-lobby.png)

