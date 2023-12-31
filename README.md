[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2023-AD272)](https://api.reuse.software/info/github.com/SAP-samples/teched2023-AD272)

# AD272 - Best of both sides: SAP Cloud Programming Model meets SAP Build

## Description

This repository contains the material for the SAP TechEd 2023 session called **AD272 - Best of both sides: SAP Cloud Programming Model meets SAP Build**.

Risk Management allows to identify enterprise risks and align them with business processes, accessing and tracking risk to organisational earnings and operations. Customizing risk management enables you to carry out the necessary configuration activities.

## Overview

This session introduces attendees how to use CAP services in SAP Build and leveraging SAP Build Apps, SAP Build Process Automation and SAP build Work Zone services of SAP Build portfolio to enhance the experience of managing and mitigating risks.


![SAP Build](/SAPBuild.jpeg)


In this scenario: <br>
- Applications are developed to create and mitigate risk using SAP Build Apps.
- Logic is added to :
  - update risks and change mitigation
  - trigger approval process
- Process is triggered to review and approve the changes in SAP Build Process Automation
- Cloud Application Model service is used to update risk details in the SAP HANA data source
- SAP Build Work Zone site is designed by adapting custom pages and integrating the application with UI integration cards
- Risk Manager access the business site to add and view risks, approve mitigations and track all the risks.
- In addition, whole process can be managed and monitored using out-of-the-box visibility

![Overview](/ad272overview.png)

## Requirements

There are no dedicated requirement for this exercise. But in case you want to gain some further knowledge around SAP Build, please feel free to attend these SAP TechEd workshops:
- Learn how to build and extend standard business process in SAP S/4HANA [AD163 - Extend Your Sales Order Process in SAP S/4HANA with SAP Build](https://github.com/SAP-samples/teched2023-AD163)
- Learn how to build a process and integrate with SAP and non-SAP systems [IN264 - Combine SAP Integration Suite and SAP Build Process Automation in HR](https://github.com/SAP-samples/teched2023-IN264)

## Exercises

- [Exercise 1 - SAP Build Apps](exercises/1_SAPBuildApps/)
    - [Exercise 1.1 - SAP Build Apps consuming SAP CAP](exercises/1_SAPBuildApps#exercise-11-consume-a-cap-service-in-sap-build-apps)
    - [Exercise 1.2 - SAP Build Apps - Trigger Process](exercises/1_SAPBuildApps#exercise-12-create-a-process-trigger)
- [Exercise 2 - SAP Build Process Automation](exercises/2_SAPBuildProcessAutomation/)
    - [Exercise 2.1 - Create business project and process](exercises/2_SAPBuildProcessAutomation#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Import SAPUI5](exercises/2_SAPBuildProcessAutomation#exercise-22-sub-exercise-2-description)
    - [Exercise 2.3 - Add SAPUI5 Form in Process](exercises/2_SAPBuildProcessAutomation#exercise-22-sub-exercise-2-description)
    - [Exercise 2.4 - Add Action to Update Risk](exercises/2_SAPBuildProcessAutomation#exercise-22-sub-exercise-2-description)
    - [Exercise 2.5 - Send Email Notification](exercises/2_SAPBuildProcessAutomation#exercise-22-sub-exercise-2-description)
- [Exercise 3 - SAP Build Apps Integration + Deployment](exercises/2_BuildAppsDeploy/)
    - [Exercise 4.1 - SAP Build Apps Deployment](exercises/2_BuildAppsDeploy#exercise-31-sap-build-apps-deployment)
- [Exercise 4 - SAP Build Work Zone](exercises/3_SAPBuildWorkZone/)
    - [Exercise 4.1 - Create and design a Site Using SAP Build Work Zone, standard edition](exercises/3_SAPBuildWorkZone#exercise-31-sub-exercise-1-description)
- [Exercise 5 - Open Risk Management Application and Start Process](exercises/4_OpenAppAndStartProcess/)
    - [Exercise 5.1 - Monitor Process](exercises/4_OpenAppAndStartProcess#exercise-42-sub-exercise-2-description)
    - [Exercise 5.2 - Approve Risks Mitigation from Inbox](exercises/4_OpenAppAndStartProcess#exercise-43-sub-exercise-3-description)



## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2023 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
