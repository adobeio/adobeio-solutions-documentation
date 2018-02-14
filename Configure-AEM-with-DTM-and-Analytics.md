# Adobe AEM with DTM and Analytics
Configure Your Adobe AEM Site for DTM and Analytics

The following instructions provide guidance on configuring Adobe Experience Manager (AEM) with Dynamic Tag Management (DTM) and Adobe Analytics. Although your AEM site may differ from the example site used below, you can use these steps as a guide for setting up your own configuration. 

These instructions include the following sections:

1. [Configure AEM with DTM](#AEM-with-DTM)

1. [Add an Alert to DTM](#Add-an-Alert)

1. [Configure AEM + DTM with Analytics](#Configure-Analytics)


## <a name="AEM-with-DTM">Configure AEM with DTM</a>

To configure AEM with DTM:


1. From your Adobe [DTM Account Dashboard](https://dtm.adobe.com), click on your company name.

    ![dtm dashboard](https://user-images.githubusercontent.com/29133525/34694472-7157a700-f484-11e7-9a63-6cb8dcb1a2db.png)


1. On the company dashboard, click the **Add Property** button.

    ![add property](https://user-images.githubusercontent.com/29133525/34694527-9e07689e-f484-11e7-922f-a26c0124037d.png)


1. On the **Create Property** form, specify a **Name** and a **URL** and click **Create Property**.

    ![create property](https://user-images.githubusercontent.com/29133525/34694566-c7bd3128-f484-11e7-8576-bef30d6b19e0.png)
    
1. On the company dashboard, use the filter field to search for the property you created in the previous step.

    ![property filter](https://user-images.githubusercontent.com/29133525/34694876-e424f3a4-f485-11e7-979b-1cba11c52ef8.png)

1. Select the property from the search results.

1. In AEM, click **Tools** > **Operations** > **Cloud** > **Cloud Services**.


1. Under **Dynamic Tag Management**, click **Configure Now**.

    ![configure now](https://user-images.githubusercontent.com/29133525/34695129-e50f2f22-f486-11e7-991d-f1845ef05b2f.png)


1. On the **Create Configuration** box, specify a **Title** and click the **Create** button.

    ![create box](https://user-images.githubusercontent.com/29133525/34695269-6f46eda6-f487-11e7-923b-44d36795d641.png)


1. On the Dynamic Tag Management Settings box that appears in DTM Settings, provide the following information:

    * API Token
    * Company
    * Property

    ![dynamic tag management settings box](https://user-images.githubusercontent.com/29133525/34695571-9f68c8a0-f488-11e7-9cf0-e3541780f1df.png)

    1. To retrieve the API token:
    
        1. Return to the DTM Dashboard and click the Profile icon and then click **DTM Account**.
        
            ![click dtm account](https://user-images.githubusercontent.com/29133525/34695898-d2b30fee-f489-11e7-9c9a-27086af832b0.png)

        1. On the DTM **Edit Account** screen, scroll to the bottom to find and copy the **API Token**.

            ![api token value](https://user-images.githubusercontent.com/29133525/34900117-9008d9d8-f7ba-11e7-828a-dd7aff6656de.png)
            
        1. After pasting the token into the **Dynamic Tag Management Settings** box, click the **Connect to DTM** button to test it.

            ![dynamic tag management settings box](https://user-images.githubusercontent.com/29133525/34885915-b2557f5a-f77e-11e7-8b9a-85b2488e772a.png)

             You should receive a message indicating that the connection is successful.
              
             ![connection successful](https://user-images.githubusercontent.com/29133525/34696324-97124dcc-f48b-11e7-8119-81965820bd52.png)


    1. To specify the **Company**, select it from the drop-down in the field.
 
    1. To specify the **Property**, select it from the drop-down in the field. If you have many properties, you may need to scroll to find it.

1. Near the bottom of the **Dynamic Tag Settings** box, deselect the **Include Production Code on Author** option.

    ![include option](https://user-images.githubusercontent.com/29133525/34886003-f5b9d4d0-f77e-11e7-811c-4fc21711c2ae.png)


1. Click the **Staging Settings** tab and deselect the **Use self hosting** option.

    ![use self hosting](https://user-images.githubusercontent.com/29133525/34886150-66f5f674-f77f-11e7-8a1a-d731944d45f2.png)


1. Click the **Production Settings** tab and deselect the **Use self hosting** option.

    ![use self hosting](https://user-images.githubusercontent.com/29133525/34886150-66f5f674-f77f-11e7-8a1a-d731944d45f2.png)


1. Click **OK**.

1. Click the **Sites** button in AEM.

1. Click the **View Properties** pop up option on the on the site you are configuring for DTM. In these instructions, we will configure the **Geometrixx Outdoors** site.

    ![sites in aem](https://user-images.githubusercontent.com/29133525/34886880-c7df7030-f781-11e7-9496-bdcae7b187d6.png)

1. Click **Cloud Services** and then click **Edit**.

    ![cloud services edit](https://user-images.githubusercontent.com/29133525/34887177-cd30457c-f782-11e7-9cca-c13fed00b2f7.png)

1. Click the **Add Configuration** drop down and select your DTM configuration.

    ![add cloud configuration](https://user-images.githubusercontent.com/29133525/34887341-655887ce-f783-11e7-925a-8b4a112ae628.png)

1. Verify that the new configuration reference for **Dynamic Tag Management** appears.

    ![new config reference](https://user-images.githubusercontent.com/29133525/34887593-44e6167c-f784-11e7-9ff9-9c765ca1e73b.png)

1. Click **Done** in the upper right corner.

1. Open a new tab in your browser and go to the local host for your AEM site.

1. Click **Sources** on the developer tools for your site and verify the DTM file information.

    ![verify dtm file](https://user-images.githubusercontent.com/29133525/34888246-bf13165a-f786-11e7-850f-846039addef5.png)

## <a name="Add-an-Alert">Add an Alert to your DTM Property</a>

To add an alert:

1. On the AEM Dashboard, click the **Web Properties** tab and specify your DTM configuration in the **Filter By** field.

    ![specify dtm from filter](https://user-images.githubusercontent.com/29133525/34888462-9d500cd4-f787-11e7-98c8-b265aac129ec.png)

1. Select your DTM configuration from the filter results and click the **Rules** tab. Click **Page Load Rules** on the left pane and then click the **Create New Rule** button.

    ![create new rule](https://user-images.githubusercontent.com/29133525/34888744-a8bed838-f788-11e7-9613-1aa4bab013ba.png)

1. For the new rule, specify the **Name** of your alert, the **Conditions** for the **Trigger** area and the **Criteria**. You can also add criteria for the rule by clicking the **Add Criteria** button and selecting the applicable browser.

    ![page load rules](https://user-images.githubusercontent.com/29133525/34890531-884ad366-f78f-11e7-95b4-3c8a8e33e2f8.png)

1. On the **Non-Sequential** tab under **Javascript/Third Party Tags**, click the **Add New Script** button.

    ![add new script](https://user-images.githubusercontent.com/29133525/34890751-60a013a2-f790-11e7-8f25-519c62aa62bc.png)

1. On the **New Javascript** form, specify a **Tag Name** and add the Javascript code you want to associate with the tag. Click **Save Code**.

    ![new javascript](https://user-images.githubusercontent.com/29133525/34890987-2261931c-f791-11e7-8aa3-421f084a30ef.png)

1. Click **Save Rule** at the bottom of the new rule form.

1. Click the **Approvals** tab.

    ![approvals tab](https://user-images.githubusercontent.com/29133525/34891556-324b5c70-f793-11e7-941c-13faa5aef922.png)

1. Click the **Approve** button at the bottom of the **Approvals** page.

1. Refresh your web site page and verify that your alert appears.


## <a name="Configure-Analytics">Configure AEM + DTM with Analytics</a>

To configure AEM + DTM with Analytics:

1. Verify that you (or the assigned user) have administrative privileges and web services credentials for the web services group. To do this:

    1. On the Reports page in Analytics, click **Admin** and then **User Management**. If you do not see the **Admin** tab, then you do not currently have administrative privileges.

        ![user management](https://user-images.githubusercontent.com/29133525/34893235-907288f4-f799-11e7-9811-d1f9b2732afc.png)

    1. On the **Users** tab, click **Edit** in the row for your user name.
    
    1. Verify the details in the <a name="Access">**Access**</a> section.
    
        ![web service access](https://user-images.githubusercontent.com/29133525/34893602-2ab3b194-f79b-11e7-8cf4-155d5bc3342d.png)

1. Configure a new report to associate with your DTM. To do this:

    1. On the **Admin** tab of the Analytics home screen, click the **Report Suites** option. 

        ![admin tab for report suites](https://user-images.githubusercontent.com/29133525/32473097-075ec802-c323-11e7-9f4e-371acf9f4914.png)


    1. On the **Reports Suites Manager** page, click **Create New** and select **Report Suite**. Configure the new report suite so that it is accessible in Adobe Analytics and contains sufficient conversion variables (evars).
    
        ![report suite manager](https://user-images.githubusercontent.com/29133525/32474884-36e55ee8-c32c-11e7-8a50-928b73efb2f8.png)

    For more information on configuring new Report Suites, see the [Adobe Reports Suite Manager help](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. In AEM, create a new tool for Adobe Analytics. To do this:

    1. On the **Overview** tab in AEM, click the **Add a Tool** button.
    
        ![add a tool button](https://user-images.githubusercontent.com/29133525/34897601-0d61e3ca-f7ac-11e7-9139-600de6f76ccc.png)

    1. On the **Add a Tool** form, specify the following:
    
        * For **Tool Type**: Adobe Analytics
        * A **Tool Name** 
        * For **Configuration Method**: Automatic
        * For **Authenticate  via**: Web Services
        * For **Web Services Username**: The username shown in the [**Web Service Credentials** box of the administrative access section](#Access) you verified in a previous step
        * For **Shared Secret**: The secret shown in the [**Web Service Credentials** box of the administrative access section](#Access)  you verified in a previous step
     
     1. Click the **Create Tool** button.
     
        ![create tool form](https://user-images.githubusercontent.com/29133525/34898821-4fcf2154-f7b2-11e7-8a24-952d49638013.png)

1. Specify the **Staging** and **Production Report Suites** and click **Save Changes** at the bottom of the page.

    ![report suite specification](https://user-images.githubusercontent.com/29133525/34899149-5a41d0d0-f7b4-11e7-85de-a987d9e43b31.png)

1. Click the **Approvals** tab and approve the changes.

1. On your site, open the developer tools, click the **Network** tab then select the **Preserve log** option and then refresh the page. You should find that Analytics calls are successful by reviewing the response code and the log details.

    ![log details](https://user-images.githubusercontent.com/29133525/34899705-bb8dd4a8-f7b7-11e7-8d4e-baafa6add06d.png)

1. Perform various tasks and web behaviors on your site to generate Analytics data.

1. Click the **Reports** tab in Analytics and select a metric related to the behaviors you performed on your site.

    ![report metrics](https://user-images.githubusercontent.com/29133525/34899918-05b87226-f7b9-11e7-90db-2bef88f4cc24.png)

1. Make sure your report name is specified and then view the analytics data that is captured in the report. You should see it correspond with the web behavior you performed on your site.

    ![pages report](https://user-images.githubusercontent.com/29133525/34900385-bc79192c-f7bc-11e7-8779-39e8a8b2ebf0.png)

## Author

- John Wight [@johnwight](https://github.com/johnwight).
