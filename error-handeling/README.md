# 405 - HTTP verb used to access this page is not allowed." 

Steps:  
1. Open WebDav Authoring Rules and then select Disable WebDAV option present on the right bar.

2. Select Modules, find the WebDAV Module and remove it.

3. Select HandlerMapping, find the WebDAVHandler and remove it.

4. also remove   ```  <_TargetId>IISWebDeploy</_TargetId> ```  from  publishish profile so that it dowsnt accoure everytime u publish