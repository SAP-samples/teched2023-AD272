# Exercise 4 - Open Risk Management Application and Start Process

In this exercise, we will create connect all the SAP Build artificats and run the application.

## Exercise 4.1 SAP Build Apps Deployment

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


## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
