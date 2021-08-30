[title]: # (Setup JDBC Driver)
[tags]: # (setup, windows)
[priority]: # (301)
# Setup JDBC Driver Proxy Jar (Windows)

1. __Stop__ the tomcat service from Services.

   ![Stop](images/60e3d80489af31470f531d3552c205bd.png)
1. Unzip the __ThyceJDBCProxy.zip__ file and you will get the following jar files in that folder.

   * SetupUtility.jar
   * Thycen-Jdbc-Proxy.jar

1. Run the __SetupUtility.jar__.

   >**Note:** The `SetupUtility.jar` file must run on the system where you have the java application deployed.

1. Run the following command: `Run as a admin`.
1. Go to the `ThycenJDBCProxy directory`.
1. Run the following command: `Java -jar SetupUtility.jar`.

1. Enter the __Secret Server URL__, __Secret Server Username__, __Password of the Secret Server account__, and __Lib path__ of the apache tomcat server. Please see the Following screenshot:  

   ![tomcat server](images/5c9a95e524180b8038ed429d28abe914.png)
1. Use the SetupUtility to encrypt the Secret Server credentials and create the __ThycenJDBC.properties__ in the current folder.

1. Copy the `Thycen-Jdbc-Proxy.jar` file and `ThycenJDBC.properties` file into tomcat server `lib folder` located at `C:\Program Files\Apache Software Foundation\Tomcat 10.0\lib`.

   ![Files](images/a7ffa89f9059f2919f862311e26d4912.png)
1. __Start__ the tomcat server.
1. Run your java application and verify the database connection.
