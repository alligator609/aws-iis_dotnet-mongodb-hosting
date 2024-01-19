1. First If you are using AWS then in security group add custom TCP inbound rule for port 8172 
2. Then try to use the following command to see if there is port 8172 information in windows:
```
netstat -aon | findstr :8172  
```

3. If not, your port 8172 is not open, you can try the following steps:

    1. Open IIS and in the center pane, under Management, double-click Management Service.
    2. In the center pane, select Enable remote connections.
    3. In the Actions pane, click Start to start the Web Management Service.
    4. If you're prompted to save your settings, click Yes.
    <img src="/assets/iis_management1.png" alt="create vpc">

4. By default, the IIS Web Management Service listens on TCP port 8172. If Windows Firewall is enabled on your web server, you'll need to create a new inbound rule to allow TCP traffic on port 8172 (all outbound traffic is permitted by default in Windows Firewall). For more information on configuring rules in Windows Firewall, see Configuring Firewall Rules.