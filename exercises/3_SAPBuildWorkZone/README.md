
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

The site you will design will have a space and a page.



### Open SAP Build Work Zone, standard edition
Open SAP Build Work Zone, standard edition,  with this link:  [SAP Build Work Zone, standard edition](https://ad272-rt8pv9xc.dt.launchpad.cfapps.eu10.hana.ondemand.com/sites#Site-Directory).

SAP Build Work Zone should open.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/0_std_open.jpg)


## Create a site
When you access the SAP Build Work Zone, standard edition, the Site Directory is in focus. From here you’ll create your new site.

In the side panel, you’ll see four tools. The Site Directory where you’re going to create a new site. All sites that you create will be displayed here. The Content Manager where you’ll manage cross-site content such as business apps. The Channel Manager where you manage different channels that expose business content that you can integrate into your sites. The fourth icon opens Settings where you can configure various settings related to your subaccount.

1. Click **Create Site**.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/1_create_new_site.png)

2. Enter JobCore_id as the site name and click Create. id is a unique id you should use to identify your site.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/2_name_site.png)

You’ve just created a site called JobCore.

## Select the Spaces and Pages - New Experience view mode

When you create a site, you are directed to the Site Settings screen where you can edit the site settings. In this screen, you’ll select the new experience view mode. This is also where you  will assign roles to your site.

By enabling Spaces and Pages – New Experience view mode, you’ll be able to create spaces and pages locally in dedicated editors. You will be able to design your pages by adding sections with UI integration cards and app tiles. If you integrate spaces and pages from remote content providers, they will be displayed side by side with spaces you create.

1. Click Edit in the top right corner of the screen.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/4_edit_site_settings.png)

2. Under **Display**, select **Spaces and Pages - New Experience**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/5_select_new_experience.png).

3. Click **Save**

### Navigate back to the Site Directory to view the site tile.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/6-to-site-directory.png).

Your site is empty for now. In the next tutorials, you’re going to add your app and cards to your site.

## Integrate your app to SAP Build Work Zone

### Fetch updated content using the Channel Manager

1. Click the Channel Manager icon to view any available content providers.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/21-open-provider-manager.png)

2. Select the HTML5 Apps content provider.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/22-HTML5-provider.png)

3. Click refresh on the HTML5 repository

![Work Zone](/exercises/3_SAPBuildWorkZone/images/23-fetch-updated-content.png)

The HTML5 Apps content provider should now expose any newly deployed app for integration.

### Add your deployed app to your content
1. Click the icon in the side panel to open the Content Manager.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/24-open-content-editor.png)

The Content Manager shows your current Content. Navigate the Content Explorer where you can explore exposed content from available content providers, select the content, and add it to your own content.

2.  Click the Content Explorer to explore content from the available content providers.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/25-content-explorer_replace.png)

3.  Select the HTML5 Apps provider.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/26-select-HTML5-tile.png)

4.  You’ll see that your app that you’ve just deployed in SAP Build Apps, already exists in this provider. Select it and click + Add to My Content.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/27-add-app-my-content_replace.png)

5. Click the Content Manager to navigate back from the Content Explorer
![Work Zone](/exercises/3_SAPBuildWorkZone/images/28-content_manager.png)

Note that your app is in the list of content items.

Later, you’ll assign your app to the Everyone role. This is a default role - content assigned to the Everyone role is visible to all users.  

## Design your site

### Create and design a page.

1. Open the Content Manager.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/31-open-content-manager.png)

2. Click **Create** and from the dropdown list, select **Page**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/32-create-page_replace.png)

3. Enter a title for the page: **Overview_id**, Where id is your unique id, and click on **Add Section** 
![Work Zone](/exercises/3_SAPBuildWorkZone/images/33-enter-title.png)

4. Keep the section a title empty and click Add Widget.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/34-section-title.png) 

5. In the Add Widgets screen, click **Cards**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/35-select-cards.png) 

6. Select the **AD272header** card to add it to this section
![Work Zone](/exercises/3_SAPBuildWorkZone/images/36-select-card-header.png) 

7. Click the **+** sign to add another ection

![Work Zone](/exercises/3_SAPBuildWorkZone/images/37-add-section.png) 

8. Give the section a title **Risks** and click **Add Widget**.

![Work Zone](/exercises/3_SAPBuildWorkZone/images/38-added-section.png) 

9. In the Add Widgets screen, click **Tiles**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/39-select-tiles.png)

10. Select your app tile and click **Add**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/40-app-add.png)


11. Click **Add Widget** in the same section
![Work Zone](/exercises/3_SAPBuildWorkZone/images/41-widget-add.png)

12. Select **cards**
![Work Zone](/exercises/3_SAPBuildWorkZone/images/35-select-cards.png) 

13. Select risks card and click **Add**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/43-risks-add.png)

14. Hover over the Apps widget and click the + icon to add another app

![Work Zone](/exercises/3_SAPBuildWorkZone/images/Add_My_Inbox_1.png)

15. Selece the MyInbox app 
![Work Zone](/exercises/3_SAPBuildWorkZone/images/Add_My_Inbox_2.png)

16. Click **Save**
![Work Zone](/exercises/3_SAPBuildWorkZone/images/44-risks-add.png)

17. Click the **Content Manager** to navigate back to the Content Manager
![Work Zone](/exercises/3_SAPBuildWorkZone/images/45-content-manager.png)

### Create a space.
1. In the **Content Manager** click Create and then select **Space**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/46-add-space.png)

2. Enter a title for the space: **Home_id**, where id is your unique id, enable your page in this space, and click **Save**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/47-save-space.png)

3. Go back to the Content Manager using the breadcrumbs at the top. You’ll see that the space you created is added to the list of content items.

### Assign your app and space to a role
In this step, you’ll assign your space and app to the Everyone role.

Spaces and apps are assigned to a role. Users assigned to a specific role are able to access the space and see the relevant pages assigned to it. Content assigned to the Everyone role is visible to all users.

1. From the Content Manager, click the Everyone role.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/51-everyone-role.png)

2. Click **Edit**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/51-everyone-role-edit.png)

3. Under the Apps tab, you’ll see the your app that you deployed. Click the toggle to assign the this app to the role. Then click Spaces tab
![Work Zone](/exercises/3_SAPBuildWorkZone/images/52-select-app.png)

4. Under the Spaces tab, you’ll see the **Home_id** space you just created. Click the toggle to assign the **Home** space to the role. Then click **Save**.
![Work Zone](/exercises/3_SAPBuildWorkZone/images/53-select-space.png)


## Assign the cards role to your site
1. Navigate to the Site Directory
![Work Zone](/exercises/3_SAPBuildWorkZone/images/60-site-directory.png)

2. Select the cogwheel icon of your site, to view your site settings
![Work Zone](/exercises/3_SAPBuildWorkZone/images/61-site-settings.png)

3. Click **Edit** to edit your site settings
![Work Zone](/exercises/3_SAPBuildWorkZone/images/62-site-settings.png)
   
4. Add the AD272 Content Package role to the site. This role is needed to allow users access to that were added for you on this environment

![Work Zone](/exercises/3_SAPBuildWorkZone/images/63-package-role.png)

5. Make sure that the AD272 Content Package role is assigned to your site, and Click **Save**
![Work Zone](/exercises/3_SAPBuildWorkZone/images/63-package-role.png)

You now completed designing your site. In the next tutorial you will experience the site as end users will experience it.
