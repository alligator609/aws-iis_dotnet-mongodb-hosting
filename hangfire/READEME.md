To summarize the article linked in my previous reply:

In Server Manager on the server where you will run the Hangfire application, install the "Application Initialization" module (under "Web Server"-"Web Server"-"Application Development") [this might require a reboot].
<img src="/assets/hangfire-step-1.png" alt="">

In IIS, create a new application pool for your site/application, set the .NET CLR version to v4.0, set start mode to "Always Running", and set Idle Time-Out (minutes) to 0.
<img src="/assets/hangfire-step-2-2.png" alt="">

In IIS for your website that's running your Hangfire application, set the application pool to the one you created above, and set "Preload Enabled" to true.

<img src="/assets/hangfire-step-3.png" alt="">

In web.config / Configuration Editor system.webServer/applicationInitialization

doAppInitAfterRestart changed to true then apply

<img src="/assets/hangfire-step-4.png" alt="">

<a href="https://github.com/HangfireIO/Hangfire/issues/2426"> Check URL </a>

<a href="https://docs.hangfire.io/en/latest/deployment-to-production/making-aspnet-app-always-running.html#:~:text=Right%2Dclick%20on%20the%20same,waiting%20for%20the%20initial%20request."> Check Official Documentation </a>
