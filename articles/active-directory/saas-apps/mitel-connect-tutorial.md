---
title: 'Tutorial: Azure Active Directory integration with Mitel Connect | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Mitel Connect.
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: barbkess

ms.assetid: 204f540b-09f1-452b-a52f-78143710ef76
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: tutorial
ms.date: 05/03/2019
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with Mitel MiCloud Connect

In this tutorial, you will learn how to use the Mitel Connect app to integrate Azure Active Directory (Azure AD) with Mitel MiCloud Connect or CloudLink Platform. The Mitel Connect app is available in the Azure Gallery. Integrating Azure AD with MiCloud Connect or CloudLink Platform provides you with the following benefits:

* You can control user’s access to MiCloud Connect apps and to CloudLink apps in Azure AD by using their enterprise credentials.
* You can enable users on your account to be automatically signed-in to MiCloud Connect or CloudLink (single sign-on) using their Azure AD accounts.


If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis).
If you don't have an Azure subscription, [create a free account](https://azure.microsoft.com/free/) before you begin.

## Prerequisites

To configure Azure AD integration with MiCloud Connect or CloudLink platform, you need the following items:

* An Azure AD subscription

  If you don't have an Azure AD environment, you can get a [free account](https://azure.microsoft.com/free/)
* A Mitel MiCloud Connect account or Mitel CloudLink Account, depending on the application you want to configure.

## Scenario description

In this tutorial, you'll configure and test Azure AD single sign-on (SSO).

## Adding Mitel Connect from the gallery

To configure the integration of Mitel Connect into Azure AD, you need to add Mitel Connect from the gallery to your list of managed SaaS apps in the Azure portal.

* The Mitel Connect app supports **SP** initiated single sign-on.

**To add Mitel Connect from the gallery, do the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory**. The **Azure Active Directory** panel opens.

2. In the **Azure Active Directory** panel, select **Enterprise Applications**. The **All Applications** page opens, displaying a list of applications in your Azure AD tenant.

3. Click **New application**. The **Add an application** page opens. 

4. In the **Add from the gallery** section, type **Mitel Connect** in the **Enter a name** field. Click the **Mitel Connect** application from the results panel, and then click **Add** from the **Add app** panel that opens.


## Configure and test Azure AD single sign-on

In this section, you'll configure and test Azure AD single sign-on with MiCloud Connect or CloudLink Platform based on a test user named ***Britta Simon***. For single sign-on to work, a link relationship between the user in Azure AD portal and the corresponding user on the Mitel platform. Refer to the following sections for information about configuring and testing Azure AD SSO with MiCloud Connect or CloudLink Platform.

 - **[Configure and test Azure AD SSO with MiCloud Connect](#configure-and-test-azure-ad-sso-with-micloud-connect)**
 - **[Configure and test Azure AD SSO with CloudLink Platform](#configure-and-test-azure-ad-sso-with-cloudlink-platform)**

### Configure and test Azure AD SSO with MiCloud Connect

To configure and test Azure AD single sign-on with MiCloud Connect, complete the following steps:

1. **[Configure MiCloud Connect for SSO with Azure AD](#configure-micloud-connect-for-single-sign-on-with-azure-ad)** - to enable your users to use this feature and to configure the single sign-on settings on the application side.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD SSO with **Britta Simon**.
3. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable **Britta Simon** to use Azure AD SSO.
4. **[Create a Mitel MiCloud Connect test user](#create-a-mitel-micloud-connect-test-user)** - to create a user for **Britta Simon** in the MiCloud Connect account that is linked to the corresponding user in the Azure AD portal.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

#### Configure MiCloud Connect for single sign-on with Azure AD

This section describes how to enable Azure AD SSO for MiCloud Connect in the Azure portal and how to configure your MiCloud Connect account to allow single sign-on using Azure AD.

To configure MiCloud Connect for single sign-on with Azure AD, it is recommended that you  open the Azure portal and the Mitel Account portal side-by-side as you will need to copy some information from the Azure portal to the Mitel Account portal and vice versa.

1. To access the **Basic SAML Configuration** page in the [Azure portal](https://portal.azure.com/), do the following:

    a. Navigate to **Azure Active Directory** > **Enterprise applications**, and select **Mitel Connect** from the list. The **Mitel Connect Overview** page opens.

    b.	Under the **Manage** section, select **Single sign-on**.
    c. In the **Select a Single sign-on method** page that opens, click **SAML**.
	
	The **SAML-based Sign-on** page opens, displaying the **Basic SAML Configuration** section.

2. To open the configuration dialog in the Mitel Account portal, do the following:

    a. On the **Phone System** menu, click **Add-On Features**.

    b. To the right of **Single Sign-On**, click **Activate** or **Settings**.
    
    The **Connect Single Sign-On Settings** dialog box appears.
	
3. Select the **Enable Single Sign-On** check box.
    ![image](./media/mitel-connect-tutorial/Mitel_Connect_Enable.png)

4. In the Azure portal, from the **SAML-based Sign-on** page, click the Edit icon ( ) in the **Basic SAML Configuration** section. The **Basic SAML Configuration** panel opens.

5.  Copy the URL from the **Mitel Identifier (Entity ID)** field in the Mitel Account portal and paste it into the **Identifier (Entity ID)** field in the Azure portal.

6. Copy the URL from the **Reply URL (Assertion Consumer Service URL)** field in the Mitel Account portal and paste it into the **Reply URL (Assertion Consumer Service URL)** field in the Azure portal.  
   ![image](./media/mitel-connect-tutorial/Mitel_Azure_BasicConfig.png)

7. In the **Sign on URL** text box, type one of the following URLs:

    * **https://portal.shoretelsky.com** - to use the Mitel Account portal as your default Mitel application
    * **https://teamwork.shoretel.com** - to use Teamwork as your default Mitel application

    **NOTE**: The default Mitel application is the application accessed when a user clicks on the Mitel Connect tile in the Access Panel. This is also the application accessed when doing a test setup from Azure AD.

8. Click  in the **Basic SAML Configuration** panel in the Azure portal.

9. In the **SAML Signing Certificate** section on the **SAML-based sign-on** page in the Azure portal, click **Download** beside **Certificate (Base64)** to download the **Signing Certificate**. Save the certificate on your computer.
    ![image](./media/mitel-connect-tutorial/Azure_SigningCert.png)

10. Open the Signing Certificate file in a text editor, copy all data in the file, and then paste the data in the **Signing Certificate** field in the Mitel Account portal. 
    ![image](./media/mitel-connect-tutorial/Mitel_Connect_SigningCert.png)

11. In the **Setup Mitel Connect** section on the **SAML-based sign-on** page of the Azure portal, do the following:

    a. Copy the URL from the **Login URL** field and paste it into the **Sign-in URL** field in the Mitel Account portal.

    b. Copy the URL from the **Azure AD Identifier** field and paste it into the **Entity ID** field in the Mitel Account portal.
    ![image](./media/mitel-connect-tutorial/Mitel_Azure_SetupConnect.png)

12. Click **Save** on the **Connect Single Sign-On Settings** dialog box in the Mitel Account portal.

#### Create an Azure AD test user 

This section describes how to create a test user named Britta Simon in the Azure portal.

1. In the Azure portal, in the left pane, navigate to **Azure Active Directory** > **Users** > **All users**.

    ![The "Users and groups" and "All users" links](common/users.png)

2. Click **New user** at the top of the screen.

    ![New user Button](common/new-user.png)

3. In the **New user** details page that opens, enter the following details:

    a. In the **User name** field, type **BrittaSimon@<yourcompanydomain>.<extension>**.
        For example, BrittaSimon@contoso.com.
  
    b. In the **Name** field, type **Britta Simon**.

    c. In the **Password** section, do one of the following:
	    i.	Select the **Show Password** check box, and then note down the auto-generated password that is displayed in the **Initial password** box. 
		ii.	Select the **Let me create the password** option to create your own password.
		**NOTE:** This is the password a user must provide to log in to the Azure portal for the first time. 
		
    d. Click **Create**.

#### Assign the Azure AD test user

This section describes how to enable Britta Simon to use Azure SSO by granting this user access to Mitel Connect.

1. In the **Azure Active Directory** panel, select **Enterprise applications**. The **All applications** page opens, displaying a list of applications in your Azure AD tenant.

2. In the applications list, click **Mitel Connect**. The **Mitel Connect Overview** page appears.

3. In the menu on the left, click **Users and groups**. The **Users and groups** page opens.

4. Click **Add user**, then click **Users and groups** in the **Add Assignment** page that opens.

5. In the **Users and groups** page that opens, select **Britta Simon** from the **Users** list and then click **Select** at the bottom of the screen.

6. By default, the role of a new user is **Default Access**. If you are expecting any role value in the SAML assertion, select the appropriate role for the user from the list in the **Select Role** option, and then click **Select** at the bottom of the screen. 

7. In the **Add Assignment** page, click **Assign**.

#### Create a Mitel MiCloud Connect test user

This section describes how to create a user named Britta Simon on your MiCloud Connect account. Users must be created and activated before using single sign-on.

For details about adding users in the Mitel Account portal, see the [Adding a User](https://oneview.mitel.com/s/article/Adding-a-User-092815) article in the Mitel Knowledge Base.

Create a user on your MiCloud Connect account with the following details:

  * **Name:** Britta Simon

* **Business Email Address:** `brittasimon@<yourcompanydomain>.<extension>`   
(Example: [brittasimon@contoso.com](mailto:brittasimon@contoso.com))

* **Username:** `brittasimon@<yourcompanydomain>.<extension>`  
(Example: [brittasimon@contoso.com](mailto:brittasimon@contoso.com); the user’s username is typically the same as the user’s business email address)

**NOTE:** The user’s MiCloud Connect username must be identical to the **User Principal Name** in Azure.

#### Test single sign-on

This section briefs how to test your Azure AD single sign-on configuration using the Access Panel.

When you click the Mitel Connect tile in the Access Panel, you should be automatically redirected to sign in to the MiCloud Connect application you configured as your default in the **Sign on URL** field. For more information about the Access Panel, see [Introduction to the Access Panel](https://docs.microsoft.com/azure/active-directory/active-directory-saas-access-panel-introduction).

### Configure and test Azure AD SSO with CloudLink Platform

To configure and test Azure AD single sign-on with CloudLink Platform, complete the following steps:

1. **[Configure CloudLink Platform for single sign-on with Azure AD](#configure-cloudlink-platform-for-single-sign-on-with-azure-ad)** - to enable your users to use this feature and to configure the single sign-on settings on the application side.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD SSO with **Britta Simon**.
3. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable **Britta Simon** to use Azure AD SSO.
4. **[Create a CloudLink test user](#create-a-cloudlink-test-user)** - to have a corresponding user for **Britta Simon** in the CloudLink account that is linked to Britta Simon in Azure AD.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

#### Configure CloudLink Platform for single sign-on with Azure AD

This section describes how to enable Azure AD SSO for CloudLink platform in the Azure portal and how to configure your CloudLink platform account to allow single sign-on using Azure AD.

To configure CloudLink platform with single sign-on for Azure AD, it is recommended that you  open the Azure portal and the CloudLink Accounts portal side-by-side as you will need to copy some information from the Azure portal to the CloudLink Accounts portal and vice versa.

1. To access the **Basic SAML Configuration** page in the [Azure portal](https://portal.azure.com/), do the following:

    a. Navigate to **Azure Active Directory** > **Enterprise applications**, and select **Mitel Connect** from the list. The **Mitel Connect Overview** page opens.

    b.	Under the **Manage** section, select **Single sign-on**.
    c. In the **Select a Single sign-on method** page that opens, click **SAML**.
	
	The **SAML-based Sign-on** page opens, displaying the **Basic SAML Configuration** section.

2. To access the **Azure AD Single Sign On** configuration panel in the CloudLink Accounts portal, you must do the following:

    a. Navigate to the **Account Information** page of the customer account with which you want to enable the integration.

    b. In the **Integrations** section, click **+ Add new**. A pop-up screen displays the **Integrations** panel.
    
    c. Click the **3rd party** tab. A list of supported third-party applications is displayed. Click the **Add** button associated with **Azure AD Single Sign On**, and click **Done**. 
    The **Azure AD Single Sign On** is enabled for the customer account and is added to the **Integrations** section of the **Account Information** page. 
    
	d. Click **Complete setup**.
	 The **Azure AD Single Sign On** configuration panel opens.
	 Mitel recommends that the **Enable Mitel Credentials (Optional)** check box in the **Optional Mitel credentials** section is not selected. Select this checkbox only if you want the user to log in to the CloudLink application using the Mitel credentials in addition to the single sign-on option. 
	
3. In the Azure portal, from the **SAML-based Sign-on** page, click the Edit icon ( ) in the **Basic SAML Configuration** section. The **Basic SAML Configuration** panel opens.

4.  Copy the URL from the **Mitel Identifier (Entity ID)** field in the CloudLink Accounts portal and paste it into the **Identifier (Entity ID)** field in the Azure portal.

5. Copy the URL from the **Reply URL (Assertion Consumer Service URL)** field in the CloudLink Accounts portal and paste it into the **Reply URL (Assertion Consumer Service URL)** field in the Azure portal.  
   ![image](./media/mitel-connect-tutorial/Mitel_Azure_BasicConfig.png)

6. In the **Sign on URL** text box, type one of the following URLs:

    * **https://accounts.mitel.io** - to use the CloudLink Accounts portal as your default Mitel application

    **NOTE**: The default Mitel application is the application accessed when a user clicks on the Mitel Connect tile in the Access Panel. This is also the application accessed when doing a test setup from Azure AD.

7. Click  in the **Basic SAML Configuration** panel in the Azure portal.

8. In the **SAML Signing Certificate** section on the **SAML-based sign-on** page in the Azure portal, click **Download** beside **Certificate (Base64)** to download the **Signing Certificate**. Save the certificate on your computer.

9. Open the Signing Certificate file in a text editor, copy all data in the file, and then paste the data in the **Signing Certificate** field in the CloudLink Accounts portal. 

10. In the **Setup Mitel Connect** section on the **SAML-based sign-on** page of the Azure portal, do the following:

    a. Copy the URL from the **Login URL** field and paste it into the **Sign-in URL** field in the CloudLink Accounts portal.

    b. Copy the URL from the **Azure AD Identifier** field and paste it into the **Entity ID** field in the CloudLink Accounts portal.

11. Click **Save** on the **Azure AD Single Sign On** panel in the CloudLink Accounts portal.

#### Create an Azure AD test user 

This section describes how to create a test user named Britta Simon in the Azure portal.

1. In the Azure portal, in the left pane, navigate to **Azure Active Directory** > **Users** > **All users**.

2. Click **New user** at the top of the screen.

3. In the **New user** details page that opens, enter the following details:

    a. In the **User name** field, type **BrittaSimon@<yourcompanydomain>.<extension>**.
        For example, BrittaSimon@contoso.com.
  
    b. In the **Name** field, type **Britta Simon**.

    c. In the **Password** section, do one of the following:
	i.Select the **Show Password** check box, and then note down the auto-generated password that is displayed in the **Initial password** box. 
	ii.Select the **Let me create the password** option to create your own password.
	**NOTE:** This is the password a user must provide to log in to the Azure portal for the first time. 
		
    d. Click **Create**.

#### Assign the Azure AD test user

This section describes how to enable Britta Simon to use Azure SSO by granting this user access to Mitel Connect.

1. In the **Azure Active Directory** panel, select **Enterprise applications**. The **All applications** page opens, displaying a list of applications in your Azure AD tenant.

2. In the applications list, click **Mitel Connect**. The **Mitel Connect Overview** page appears.

3. In the menu on the left, click **Users and groups**. The **Users and groups** page opens.

4. Click **Add user**, then click **Users and groups** in the **Add Assignment** page that opens.

5. In the **Users and groups** page that opens, select **Britta Simon** from the **Users** list and then click **Select** at the bottom of the screen.

6. By default, the role of a new user is **Default Access**. If you are expecting any role value in the SAML assertion, select the appropriate role for the user from the list in the **Select Role** option, and then click **Select** at the bottom of the screen. 

7. In the **Add Assignment** page, click **Assign**.

#### Create a CloudLink test user

This section describes how to create a user named Britta Simon on your CloudLink platform. Users must be created and activated before using single sign-on.

For details about adding users in the CloudLink Accounts portal, see the ***Managing Users*** topic in [CloudLink Accounts documentation](https://www.mitel.com/document-center/technology/cloudlink/all-releases/en/cloudlink-accounts-html).

Create a user on your CloudLink Accounts portal with the following details:

* **Name:** Britta Simon

* **First Name:** Britta

* **Last Name:** Simon

* **Email:** BrittaSimon@contoso.com

**NOTE:** The user’s CloudLink email address must be identical to the **User Principal Name** in Azure.

### Test single sign-on

This section briefs how to test your Azure AD single sign-on configuration using the Access Panel.

When you click the Mitel Connect tile in the Access Panel, you should be automatically redirected to sign in to the CloudLink application you configured as your default in the **Sign on URL** field. For more information about the Access Panel, see [Introduction to the Access Panel](https://docs.microsoft.com/azure/active-directory/active-directory-saas-access-panel-introduction).

## Additional Resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-saas-tutorial-list)

- [What is application access and single sign-on with Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis)

- [What is Conditional Access in Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)
