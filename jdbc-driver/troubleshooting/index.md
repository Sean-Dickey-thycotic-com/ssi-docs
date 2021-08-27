[title]: # (Troubleshooting)
[tags]: # (troubleshooting)
[priority]: # (200)
# Troubleshooting

* The application account should have the __View Secret__ Permission.
* The secret created in Secret Server should have application account permission.
* Verify the __username__ and __password__ of the secret is the same as your database name.
* The Secrete Server application account user should not be locked out.
* You should check the error in __Catalina__ in below path: `C:\Program Files\Apache Software Foundation\Tomcat 10.0\logs`

>**Note:** If you put the wrong credentials for Secret Server and do not provide user permission to the secret and try to connect with your database then the following error will be occur: “Access Denied” or “Authentication fail” in Catalina at below path: `C:\Program Files\Apache Software Foundation\Tomcat 10.0\log`
