<h1>Cloud Security Project: IAM-Based EC2 Security and Access Control</h1>



<h2>Description</h2>
This project focuses on enhancing the security of cloud environments using AWS Identity and Access Management (IAM). By implementing IAM policies, I ensured that users can perform specific actions only on designated EC2 instances. I created two EC2 instances (development and production), set up a custom IAM policy using the JSON editor, and tested access controls for different actions, such as deleting EC2 instances.<br/>


<br />

<h2>Tools and Technologies Used</h2>

- **Amazon Web Services (AWS)**: The cloud platform used for this project.
- **AWS IAM (Identity and Access Management)**: Managed user access and permissions securely through custom policies.
- **Amazon EC2**: EC2 instances were used for demonstrating scalable computing and secure instance management.
- **JSON Editor**: Used to create custom IAM policies by writing permissions in JSON format.
- **IAM User Groups**: Organized users into groups to control access levels more efficiently.
- **AWS Management Console**: Used for configuring and testing IAM policies and EC2 instances.
  <br/>
  
<h2>Key Features</h2>

- **Custom IAM Policy**: Created a policy using the JSON editor that allows specific EC2 actions for instances with the "development" tag and denies actions like creating or deleting tags for all instances.

- **Secure Access Control**: Managed user permissions by assigning the policy to a user group, ensuring that only authorized actions could be performed on EC2 instances.

- **Testing Access Permissions**: Verified the effectiveness of the policy by testing access using an IAM user account, trying to delete both development and production instances.

- **Separation of Environments**: Ensured the correct access control between development and production environments to avoid accidental production data loss.


<br/>


<h2>Steps Undertaken :</h2>

  1. <b>Launched EC2 Instances:</b><br/>
     - Launched two EC2 instances through the AWS Management Console: one tagged as env: development and the other as env: production.<br/>
     </br>
    

     <img src="https://i.imgur.com/BEELawq.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
     
<br />
 2. <b>Created a Custom IAM Policy Using JSON Editor:</b><br/>
     - Created a custom IAM policy that allows all EC2 actions on instances with the environment: development tag and denies any tag modifications across all EC2 instances.<br/>
     - The policy was written using the JSON editor in IAM, and key policy details included:<br/>
         <br/>

  

<img src="https://i.imgur.com/8wpmfxG.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />


  3. <b>Created an IAM User Group and Attached the Policy:</b><br/>
      - Created a user group in IAM and attached the custom policy that I had created.<br/>
      - This group was used to manage access to resources for specific users, ensuring they only had permissions for the development environment.<br/>
        <br/>

<img src="https://i.imgur.com/zKVnp2I.png" height="90%" width="80%" alt="Disk Sanitization Steps"/>

<br />
<br />
 4. <b>Added a User to the Group:</b><br/>
   - Created a new IAM user and added them to the created group. This ensured the user inherited the permissions defined in the attached policy.<br/>
   - Allowed inbound access only from specific IP addresses. <br/>
        <br/>
       
      
     
     
<img src="https://i.imgur.com/UEYT6zY.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<br />
<br />

5. <b>Configured a Custom Sign-In Alias for the User:</b><br/>
   - To enhance user experience and security, I created an IAM account alias. This alias provided a custom sign-in URL that made the login process more intuitive for users.<br/>

  <br/>
<img src="https://i.imgur.com/lW8lPDP.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>

<br />
<br />


6. <b>Tested IAM Permissions<b/><br/>
    - Logged in to the AWS console using the IAM user account and tested the IAM permissions.<br/>
    - First attempted to delete the production EC2 instance. This action was denied due to the policy restricting actions on production instances.<br/>
    - Then attempted to delete the development EC2 instance. This action was successful, as the IAM policy allowed it for instances with the env: development tag.<br/>

  <br/>
<img src="https://i.imgur.com/dqQ8Mzt.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/t4KUL3C.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xLH0oDD.png" height="130%" width="70%" alt="Disk Sanitization Steps"/>

<br />




<h2>Key Learnings</h2>

- **IAM Policy Creation**: Gained experience in writing and deploying custom IAM policies using the JSON editor.

- **Tag-Based Permissions**: Learned how to use EC2 instance tags to control access to resources based on specific criteria.

- **Custom User Aliases**: Set up custom sign-in URLs for IAM users to improve the login process and add a layer of security.

- **Real-World Cloud Security**: This project helped me understand how to manage access in a cloud environment, applying best practices to ensure security and avoid unauthorized access.


</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
