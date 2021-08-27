[title]: # (Locate your Database configuration file)
[tags]: # (database, linux)
[priority]: # (106)
# Locate your Database configuration file (Linux)

1. __Stop__ the tomcat service from the terminal.  

   ![tomcat](images/9d31d6b1d94655a1b7458e8c334003b1.png)
1. Unzip the __ThyceJDBCProxy.zip__ file and you will get the following jar files in that folder:

   * __SetupUtility.jar__
   * __Thycen-Jdbc-Proxy.jar__
   * __Run SetupUtility.jar__

   >**Note:** The SetupUtility.jar must run on the system where you have the java application is deployed.

1. Run the terminal.
1. Go to to the `ThycenJDBCProxy directory`.
1. Run the following command: `Java -jar SetupUtility.jar`.
1. Enter the __Secret Server URL__, __Secret Server Username__, __Password of the Secret Server__, and __Lib path__ of the apache tomcat server. Please see the following screenshot:  

   ![ThycenJDBCProxy](images/3f35d7b656e6fb5f186377f682d9a96a.png)
1. Run the SetupUtility to encrypt the Secret Server credentials and create the __ThycenJDBC.properties__ in the current folder.
1. copy the __Thycen-Jdbc-Proxy.jar__ and __ThycenJDBC.properties__ into tomcat server __lib__ folder located at `/usr/share/apache-tomact/lib`.  

   ![SetupUtility](images/65e446560190596e5bf8360336dc586a.png)
1. __Start__ the tomcat from terminal.  

   ![tomcat](images/e00a2b0dd933006cb55b26e3e2a88ed2.png)
1. Run your java application and verify the database connection.

   >**Note:** Please check the tomcat server log to confirm whether your application is
using the ThycenJDBC driver proxy or not. If it is using the proxy driver in such
case it will display the following line in the logs:

   * “Using Thycen JDBC Driver”
   * “Trying to connect with secret server”
   * “Secrete fetched successfully”
