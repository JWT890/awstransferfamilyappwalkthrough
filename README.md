# awstransferfamilyappwalkthrough

The AWS Family Transfer App offers secure file transfers within organizations at a no-code approach utilizing Amazon S3 services and reduces the need to troubleshoot, install, support, and manage different file transfer clients across a spectrum of end user devices and systems through a more browser friendly approach.  
![image](https://github.com/user-attachments/assets/e124527d-d41e-4c12-b737-908f0c5bd576)

First step is to sign in to IAM Identity Center and go to settings and write down your Instance ARN for later.  
Second step is to look under related consoles and select IAM which takes you to a different tab:  
![image](https://github.com/user-attachments/assets/d1ab0f7c-c3bc-4495-a0c4-1020ea5cd290)  
![image](https://github.com/user-attachments/assets/53c28cf1-3dab-4d32-a939-2b9b4b539d9f)  

Click on Web apps tab and then click the Create Web App orange button. After clicking it, you will configure the web app. Keep everything the same as is until you get to the tags section:   
![image](https://github.com/user-attachments/assets/d712660e-716d-4d74-8ec8-9554a8e6a4ac)  
Under tags click on key and name it Name and for Value enter Transfer Family web app demo:  
![image](https://github.com/user-attachments/assets/53714d30-ed75-4929-98a7-733cadcf3f0b)
Click next and upload a logo if desired and click next. Then click create web app.  
Next click on the web app and click on assign users and groups and select assign existing uses and groups:  
![image](https://github.com/user-attachments/assets/937e0c79-db80-40a6-97d5-e4c931ec3416)  
And search for your user in IAM and click assign.  
You will then be taken back to web app details and then take note of it for later. On the users tab, take note of the User ID for later.  

Second step is to head over the Amazon S3 page and create a bucket and give it a unique bucket name and leave the rest as defaults.  
After creating the bucket, select the new bucket and go to permissions and scroll down till you see CORS and click edit:  
![image](https://github.com/user-attachments/assets/b05cd8ae-95a3-4949-ab46-6212e4cee3b4)  
Copy and paste the code:   
![image](https://github.com/user-attachments/assets/57afe6bb-664f-4c90-9b38-d088b4bec8be)
and replace the AccessEndpoint with the Instance-ARN from the prior step. Modify to include https://web-app-Instance-ARN-webapp.us-Location-Number.on.aws and then click save.  

Third step is to to head over the Amazon S3 Access Grants tab by going to the S3 tab and clicking on Access Grants:  
![image](https://github.com/user-attachments/assets/6d102645-d143-4560-af28-88ec4ecd167f)  
And clicking on Create S3 Amazon Access Grants instance. For step 1 click the checkbox for add the instance to the region your in and then enter IAM ARN from the first step and click next and then cancel.  
The Access Grants will be created. Next head to the locations tab and register a location. You will be greeted by this screen:  
![image](https://github.com/user-attachments/assets/55962086-7e4a-4556-9eef-7556433304b7)  
For scope, choose the bucket you created by selecting Browse S3 and select the created bucket.  
For IAM role choose the create new role option and click on register location to continue.  
After its created, you then want to create a grant by clicking the Create Grant orange button. After clicking it, you will want to click on browse locations and select the path of the S3 bucket and select choose path.  
For subprefix put *, permissions set to read and write, grantee type being a directory identity from IAM Center, type as User and put the user ID copied down as the input. Click on Create Grant.  





