## steps to run dotnet application in IIS
### Step 1 : install iis featuere from windows server. 
Check your all IIS Services are running on your system properly or not. If not, then open the server manger go to the program and features, and click on Add rules and feature.
<img src="/assets/server-manager.png" alt="create vpc">
Then add the following features.

<img src="/assets/WindowsFeatures.jpg" alt="create vpc">

Search for IIS and you should see it.

### Step 2: Install ASP.NET Core 6.9 Runtime – Windows Hosting Bundle Installer

### Step 3: Now you can create a new application in your IIS server and publish your Application into the newly created application.

### Fre local server IIS management services 

### Step 4: To directly publish by Visual Studio

On Windows Server, download Web Deploy 4.0.
make sure this service are added when u intall web deploy 

<img src="/assets/webdeploy.png" alt="create vpc">

### Open port 8172 to deploy via Visual studio 

### Enable Remote Connections in IIS 

Just connect to the remote server through RDP, open IIS and open this option:

<img src="/assets/iHfLN.png" alt="create vpc">

In the right panel, stop it. This will actually stop Web Management Service. 
Then you will be able to check Enable remote connections flag. Check it, click the Apply option in the right panel, then Start.

This is also necessary for enabling you to remotely connect to this IIS server from other computers (like your dev computer).

<img src="/assets/iis_management.png" alt="create vpc">

### then check if port is open. 

### Add 


