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
