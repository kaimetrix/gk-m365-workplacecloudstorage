# M365 Workplace Cloud Storage Spec
## Abstract
Microsoft cloud managed Modern Workplace devices get all relevant policies and configurations from Microsoft Intune. Some of these settings rely on files available by URL. This application is intended to manage these files with an easy to use web based approach where administrators can create and edit the files and separate the content based on groups.

## Deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fglueckkanja%2Fgk-m365-workplacecloudstorage%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

## Enabling Easy Auth (Azure AD authentication)
1. Open [Azure Portal](https://www.portal.azure.com) and navigate to the deployed **M365 Workplace Cloud Storage** app service. 
2. Select **Authentication / Authorization** under **Settings** and enable **App Service Authentication**.
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/1.png)
3. Set **Action to take when request is not authenticated** to **Log in with Azure Active Directory**.
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/2.png)
4. Configure **Azure Active Directory** as the **Authentication Provider**
    - Set **Management mode** to **Express**.
    - Create a new AD App or select an existing if you have already registered an AD App for **M365 Workplace Cloud Storage**
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/3.png)
5. Save the changes
6. Navigate to **Overview** and click the URL of **M365 Workplace Cloud Storage**
7. If Service is not starting or Authentication fails wait a few moments
8. Accept requested permissions
9. Check **Consent on behalf of your organization** if you want to accept the requested permissions for all users within your organization
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/4.png)

## Authorize users or groups
### Enable authorization for M365 Workplace Cloud Storage
1. Open [Azure Portal](https://www.portal.azure.com) and navigate to **Azure Active Directory**
2. Click **Enterprise applications** from the blade
3. Select the app you have created in the steps before
4. Click **Properties** from the **Manage** section
5. Set **User assignment required** to **Yes**

### Grant specific users and groups access to M365 Workplace Cloud Storage
1. Click **Users and groups** 
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/5.png)
2. Click **Add user**
3. You can grant access to the application to specific user or groups
![](https://github.com/glueckkanja/gk-m365-workplacecloudstorage/raw/master/docs/images/6.png)
