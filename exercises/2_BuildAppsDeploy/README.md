# Exercise 3 - SAP Build Apps Integration and Deployment

In this exercise, we will create connect all the SAP Build artificats and run the application.

## Exercise 3.1 SAP Build Apps Deployment

After completing these steps you will have created the final app which can be accessed by enduser via SAP Build Work Zone.

1. Open again your SAP Build Apps project from the lobby. Go to the Variables and change the intial value of the app variable **definitionId** to your individual definitionId from the SAP Build Process Automation exercise
<br>![](/exercises/4_OpenAppAndStartProcess/images/11a-app-variable.jpg)

2.	Now click on *LAUNCH* in the main navigation tab. Afterwards open the Build Service.
3.	Under **Web App** select the BUILD button. Choose MTAR, the highest Client runtime version and **1.0.0** as Version.
<br>![](/exercises/4_OpenAppAndStartProcess/images/11b-build.jpg)

The build may take a a little while(20 minutes or so) so you may want to skip to the next tutorial. If you refresh the page, the status will change from created to queued to finally delivered. 
As soon as it is delivered click **Deploy MTA**
<br>![](/exercises/4_OpenAppAndStartProcess/images/11c-deploy-mtar.jpg)

The first you deploy, you will get the following to sign in to Cloud Foundry so you can deploy the app.
Select endpoint cf-eu10-004 and press **Auhtorize BTP Deployments**
<br>![](/exercises/4_OpenAppAndStartProcess/images/11d-mta.jpg)

You will get a dialog for signing in to the deployment environment (Cloud Foundry).
Enter your custom IDP origin key in the input box **tdct3ched1-platform** and then click Sign in with alternative identity provider.
Once signed in, the Cloud Foundry organization to deploy the app to is selected. Now press **deploy MTA to AD272**
<br>![](/exercises/4_OpenAppAndStartProcess/images/11e-deploy-to-ad272.jpg)


## Summary

You've now inetgrated your own process into the SAP Build Apps application and deployed it for end user to Cloud Foundry.

Now we move over to SAP Build Work Zone:
[Exercise 2 - SAP Build Work Zone](exercises/3_SAPBuildWorkZone/README.md)


