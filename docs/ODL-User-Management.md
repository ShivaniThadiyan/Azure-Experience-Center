## ODL User Management
 * [User Signup type and usage](#user-signup-type-and-usage)
 * [Registration Management](#registration-management)
 * [Managing and distributing Vouchers](#managing-and-distributing-vouchers)
 * [Managing each user lab](#managing-each-user-lab)

### ODL User Management

 The ODL registration page looks as below  

<img src="/Images/ODL_reg.png"/>

**A**: The users can register for the workshop here with the required details and click on **Submit**.  
**B**: The name of the event is displayed here, which is same as the ODL name given at the time of ODL creation. It also shows the organisation which conducts the workshop with their Logo.  
**C**: This is the short description of the workshop, which is same as the description given at the time of ODL creation.  
**D**: This is the duration for which the user will have access to ODL environment.  
**E**: This is the email ID of the contact person who scheduled the workshop, which is same as given at the time of ODL creation.  
**F**: These are the tags mentioned while creating the ODL.  
**G**: This is the Custom ODL name that we mentioned at the time of ODL creation.  

### User Signup type and usage
- There are 4 type of user signup

  * Registration Required : This defines that the user should register for the ODL to get access to the ODL.  
  * Registration & Email Validation Required : This defines that the user should register for the ODL and launch the lab from the Email sent from AEC to get access to the ODL.  
  * Registration & Approval Required : This defines that the user should register for the ODL. Here the user will not be able to access the ODL unless the Instructor approves the registration from the User Window of the ODL.  
  * Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.  

### Registration Management

- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
- Once logged in, click on **ODL** on the left pane of the portal. This will list the ODLs if any.
   
 <img src="/Images/ODL_click.png"/> 
  
- Click on **Edit Icon** to edit the created ODL.  

<img src="/Images/Edit_ODL.png"/>

- In the Edit ODL page, copy the URL from the first field. This is the ODL registration page URL. The Instructor can customize this URL using bitlink before. 

<img src="/Images/ODL_URL.png"/>

### Managing and distributing Vouchers

- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.

- Once logged in, click on On Demand labs on the left pane of the portal. This will list the all ODL's if any.

<img src="/Images/Vouchers_odl.png"/>

- Navigate Test ODL that created earlier, Click on Edit Icon to edit the created ODL.For create voucher, approval will be Invite only.
* Approval : Choose only **invite only** option to define the approval type for the ODL.
   * Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.

* Enable Vouchers : Check this option if you want to genete vouchers to distribute to the users. This will be checked by default if you select the approval type as Invite Only.

- Click on **Submit** once required options above are populated.

<img src="/Images/Click_EnableVoucher.png"/>

- Click on **Vouchers** button.

<img src="/Images/Click_VoucherButton.png"/>

- Click on **Add Vouchers**.

<img src="/Images/Click_AddVouchers.png"/>

- Now provide the following details in the Add Vouchers Page that comes up.

<img src="/Images/Click_Submit.png"/>

- Now you can see the voucher added successfully.

<img src="/Images/Vouchers_addedSuccessfully.png"/>

The ODL registration page looks as below.

<img src="/Images/Registration_Page.png"/>

- The users can register for the workshop here with the required details and click on **Submit**.

**Distributing Vouchers**
- Copy the Voucher Code that you created and give in registration page.

<img src="/Images/Copy_VoucherCode.png"/>

- Paste the Voucher Code in Registration page below.

<img src="/Images/Registration_Add%20details.png"/>

- Click on **Submit** once required options are populated.

- Now you can see the registration successful.

<img src="/Images/Registration_Successfull.png"/>

- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.

- Once logged in, click on On Demand labs on the left pane of the portal. This will list the all ODL's if any.

- Click on Vouchers Button.

- Now click on **Available** button, you can see the voucher code that is available for user.

<img src="/Images/Click_Available.png"/>

- Now click on **Redeemed** button, you can see that voucher code is redeem for user.

<img src="/Images/Click_Redeemed.png"/>

### Managing each user lab
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
- Once logged in, click on **ODL** on the left pane of the portal. This will list the events if any.  

<img src="/Images/ODL_click.png"/>

- Click on **Users** of the ODL's page,This will list the users if any.

<img src="/Images/odl_users.png"/>

- Now you can see the user, Click on **Invite link**.

<img src="/Images/odl_sent_Invite.png"/>

- It will redirect the Launch Lab Page. Click on **Launch Lab**.

<img src="/Images/odl_launch_lab.png"/>

- Now you can see the your environment is creating.

<img src="/Images/odl_environment.png"/>

- Now you will get the ODL user Crendentials details.

<img src="/Images/odl_userURL.png"/>

- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials. 

- Once logged in, click on **ODL's** on the left pane of the portal.Click on users. You can see the all options after launching the lab.

- In Users, Click on **View lab status**.

<img src="/Images/odl_viewlabStatus.png"/>

- Now you can see the status.

<img src="/Images/odl_lab_viewstatus.png"/>

- In lab status Page, you can reset the password. Click on **Reset** button.

<img src="/Images/odl_reset_labpwd.png"/>

- Click OK.

<img src="/Images/odl_passwd.png"/>

- Now you can also delete the environment. Click on **Delete environment** button.

<img src="/Images/odl_delete_environment.png"/>

- Click OK.

<img src="/Images/odl_click_ok.png"/>

- It will delete successfully.

[<Previous](https://github.com/ShivaniThadiyan/Azure-Experience-Center/blob/master/docs/Creating-and-Managing-ODL%E2%80%99s.md) /
[Next>](https://github.com/ShivaniThadiyan/Azure-Experience-Center/blob/master/docs/Report.md)
