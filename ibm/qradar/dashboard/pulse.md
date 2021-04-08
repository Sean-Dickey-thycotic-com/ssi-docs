[title]: # (Pulse Dashboard Setup)
[tags]: # (dashboard)
[priority]: # (303)
# Pulse Dashboard Setup

To Configure Pulse Dashboard Setup (The QRadar integration is also available at Thycotic.com):

1. Click on __Add | Browse the pulse Zip file | Check “install immediately”__.
1. Click on the __Add__ button.  

   ![](images/c58362e449a8d57c4fc144799b087e96.png)
1. You should see the pulse QRadar pulse app in the extension management.  

   ![](images/7de5f62b944a6b91aa074cd3aa2c0f3b.png)
1. Click on the __Pulse__ Extension from the menu.

   ![](images/b3ef824c9f206b3ca4e36d24c89373cc.png)
1. Click on the dashboard dropdown and select __New Dashboard__.

   ![](images/3597bbe7e123946d5afab2fb9e253b61.png)
1. Click on __Import Dashboard__.  

   ![](images/4ae71cc31024057722b0d6c9397dd46c.png)
1. Extract the __Thycotic Secret Server dashboard zip__.

   ![](images/ffeef2daf3be3c95f7848445531eea2b.png)
1. Click on __Add File__.
1. Navigate to __Secret Server Dashboard.json__.
1. Click on the __Import__ button.

   ![](images/d33e317a6ae3f8503277f2eff73e7ec1.png)
1. The __Secret Server Dashboard__ will be displayed in Pulse.

   ![](images/1562afa88cb02d802bf26236dbe3fb22.png)

   ![](images/726c501091664c0eda7c141c325b738c.png)

## Secret Server Dashboard Widget

* Add __Log Source Name__ to the __LogSource_Thycotic__ Parameters.  

   ![](images/afc6bb0b2ea90a406d22dcd639615d81.png)
* __Heartbeat Status__  

   * __Success:__ The credentials in the Secret authenticated successfully with the target system.  
   * __Failed:__ The credentials in the Secret failed authentication with the target system.  

   ![](images/4c31da9a5fd9c3da14d5ed25c70eeea3.png)
* __Password Rotation__  

    * __Success:__ A Secret Password has changed.  
    * __Failed:__ A Secret Password has failed to change.  

   ![](images/bcb8d6d574743ea1c5eaf8cae9a9824d.png)
* __Secret expired or Soon to be expired__  

   ![](images/0a0ebf640f22f69b3b91e6fae1f03a6a.png)
* __Top 15 login user count__  

   ![](images/d154537e21088c608a7bbeb5be4a7a4b.png)
* __Top 20 Recent Administrator Activities__

   ![](images/1f923646b1f5d6524a52c1ada965355a.png)
* __Top 20 Most Used Secrets__  

   ![](images/165774985d041adb7db58929ff2b0536.png)
* __Last 30 Viewed Sessions__  

   ![](images/ba11024ae2a4b88fd4fcda60146b3c47.png)
* __Last 30 Login Failure Users__

   ![](images/b33756073003ed3f38306a31ad277900.png)
