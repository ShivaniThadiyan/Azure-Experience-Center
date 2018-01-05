## Creating AEC Templates
  * [Create Template](#create-template)
    * [Explanation of all fields](#explanation-of-all-fields)
  * [ARM Template Best Practices](#arm-template-best-practices)
    * [Use of Input Parameter functions](#use-of-input-parameter-functions)
      * [Explanation of all functions](#explanation-of-all-functions)
    * [Use of Template outputs](#use-of-template-outputs)
  * [Template Permissions](#template-permissions)
    * [Explanation with details to implement](#explanation-with-details-to-implement)
  * [Validating Template](#validating-template)
    * [Validation](#validation)
    
 ### Create Template
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
- Once logged in, click on **Templates** on the left pane of the portal. This will list the templates if any.  

<img src="/Images/templates.png"/>

- Click on **ADD** at the top right corner of the templates page, to add a new template.  

<img src="/Images/add_template.png"/>

- Now provide the following details in the Add Template page that comes up.  
### Explanation of all fields
* **Name:** Provide a suitable name to the template.
* **Code**: Provide an identifyable course code.
* **Description:** Enter the description of the template.  
* **ARM Template URL(optional):** Upload the ARM template that automate the required resources for the event, to storage and provide the template link.  
* **Parameter Template URL(optional):** Upload the parameter template that is used in the ARM template, to storage and provide the parameter template link.  
* **Owner Email:** Provide the email ID of the owner of the workshop.  
* **Deployment Plan:** Choose any of the deployment plan as below
  * **Single Resource Group:** Choose this plan if you need only one resource group for the workshop to deploy.
  * **Shared Instance:** Choosing this plan will provide one resource group for all the attendees in the workshop.
  * **Resource Group-Two:** Choose this plan if you need two resource group for the workshop to deploy.
  * **Resource Group-Three:** Choose this plan if you need three resource group for the workshop to deploy.
  * **Resource Group-Four:** Choose this plan if you need four resource group for the workshop to deploy.   
  * **Resource Group-Five**: Choose this plan if you need five resource group for the workshop to deploy.

* **Lab Guide URL(optional):** Upload the lab guide for the workshop, to storage and provide the lab guide link. 
* **Demo URL(optional):** Provide the link to sample or quickstart.  
* **PPT URL(optional):** Provide link to presentation slides.  
* **Prerequisites URL(optional):** Provide the link to prerequisites URL(if any).  
* **Regions:** Provide the regions where you want to deploy the template.
* **MS Cloud Licenses(optional):** Choose the license which you want to assign to the user for the lab.
* **Create Service Principal(optional):** Check this option if you want to create separate service principle for each of the users registered for the lab.
* **Send Service Principal(option comes up only if you check the above option):** Check this option if you want to send the service principle details to each of the users registered for the lab. The details will be sent with the lab details.
* **Attendee Custom RBAC URL(optional):** Create custom RBAC policies for the attendees in the workshop and upload in storage. Provide the link to policy here. 

- Click on **Submit** once required options above are populated.

<img src="/Images/add_template_details.png"/>

### ARM Template Best Practices
### Use of Input Parameter functions
### Explanation of all functions
* **GEN-PASSWORD:** Generates the  unique password for the template to deploy.
* **GEN-UNIQUE:** Generates the unique set of characters for the template to deploy.
* **GEN-UNIQUE-[Length]:** Generates a unique set of characters of the specified length so if its given as **GEN-UNIQUE-6**, then it generates 6 unique characters. This can be used as special identifiers.
* **GEN-SSH-PUB-KEY:** Genarates the SSH public key for the template to deploy.
* **GEN-GUID:** Generates a GUID, a **GUID** is a globally unique identifier, and it typically is 32 characters.
* **GET-SERVICEPRINCIPAL-NAME:** Using this function, you can get the Service-Principal-Name.
* **GET-SERVICEPRINCIPAL-SECRET:** Using this function, you can get the Service-Principal Secret key.
* **GET-SERVICEPRINCIPAL-APPLICATION-ID:** Using this function, you can get the Service-Principal Application-ID.
* **GET-SERVICEPRINCIPAL-OBJECT-ID:** Using this function, you can get the Service-Principal Object-ID.
* **GET-AZUSER-UPN:** Using this function,you can get the generated AD email of the attendee. for **example: demouser_spektrasystems_com@spektrahol.onmicrosoft.com**
* **GET-AZUSER-PASSWORD:** Using this function,you can get the temporary password of the generated AD.
* **GET-PARAMETER-FILE-BASEURI:** Using this function, you can get the Parameter-file BaseURI.
* **GET-TEMPLATE-FILE-BASEURI:** Using this function, you can get the Template-file BaseURI.
### Use of Template outputs
- If you want to provide the attendees some results that are required in the workshop, you can provide it by using an output section in the ARM template. The results can also be sent as email to the attendees when the template deployment is completed.  

### Template Permissions

- Click on **Edit Icon** to edit the created template and add the template permissions if any

<img src="/Images/Template_Edit.png"/>

### Explanation with details to implement 
* **Permission Type:** Choose any of the permission type as below
  * **Azure Built-in Role:** Choose this permission type to assign the Azure Built-in Role to the Attendee/Instructor of the workshop.
   * **Profile Type:** Choose attendee or instructor according to whom you want to assign this permission.
   * **Identity:** Choose AAD user or AAD Service Principle according to where you want to apply this permission.
   * **Scope Type:** Choose Azure to set this permission scope level at Azure
   * **Scope Level:** Choose scope level as RG level or subscription level to set the scope level of this permission.
   * **Permission:** Choose the permission as Reader or owner or contributor from the drop down according to what permission you want to assign to the Attendee/Instructor.
   * **Apply at Launch:** Check this option if you want to apply the permission at the time of deployment of the template

- Click on **Submit** once required options above are populated.
 
<img src="/Images/Azure_built-in_role.png"/>

 * **Custom ARM Policy:** Choose this permission type to assign the Custom ARM Policy to whoever is using the Resource group or Subscription of the workshop.
   * **Scope Type:** Choose Azure to set this permission scope level at Azure
   * **Scope Level:** Choose scope level as RG level or subscription level to set the scope level of this policy you are going to upload.
   * **Permission Data:** Enter the Custom policy URL of where you have uploaded the policy file. These policies will be applied to the users using the workshop according to the scope Level.
   * **Apply at Launch:** Check this option if you want to apply the policy at the time of deployment of the template

- Click on **Submit** once required options above are populated.
 
<img src="/Images/Custom_policy.png"/>

* **Azure Custom Role:** Choose this permission type to assign the Azure Custom Role to the Attendee/Instructor of the workshop.
  * **Profile Type:** Choose attendee or instructor according to whom you want to assign this role.
  * **Identity:** Choose AAD user or AAD Service Principle according to where you want to apply this custom role.
  * **Scope Type:** Choose Azure to set this custom role scope level at Azure
  * **Scope Level:** Choose scope level as RG level or subscription level to set the scope level of this custom role.
  * **Permission Data:** Enter the Custom permission URL of where you have uploaded the RBAC file. These roles will be applied to the Attendee/Instructor according to the scope Level.
  * **Apply at Launch:** Check this option if you want to apply the custom role at the time of deployment of the template

- Click on **Submit** once required options above are populated.
 
<img src="/Images/custom_role.png"/>

- Once all the permissions are added to the template, please click on **Submit** above the template permissions section.  

<img src="/Images/permissions_template.png"/>

### Validating Template
### Validation
- Click on **Validate subscription with ARM template** icon corresponding to the template created.  

<img src="/Images/Template_validate.png"/>

- Provide the azure subscription group and subscription in which the validator should be run. Also provide the regions where you want to validate the template and click on **Submit**.  

<img src="/Images/validation_details.png"/>

[<Previous](https://github.com/ShivaniThadiyan/Azure-Experience-Center/blob/master/docs/Getting%20Started.md) /
[Next>](https://github.com/ShivaniThadiyan/Azure-Experience-Center/blob/master/docs/Creating-and-Managing-ODL%E2%80%99s.md)


