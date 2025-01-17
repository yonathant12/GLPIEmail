<h1>GLPI Email Integration</h1>

<h2>Overview</h2>
In this part of the project, implemented email integration to enable automatic ticket generation and real-time updates, improving the efficiency of the ticketing system. It also provided automatic status updates to users, keeping them informed throughout the resolution process. 
<br />


<h2>Application Used</h2>

- <b>VMware Workstation 17 Pro</b>
- <b>Windows Server 2019</b>
- <b>Wampserver</b>
- <b>GLPI</b>


<h2>Lab walk-through:</h2>

<p align="left">
Select the Setup option, then click on Notifications.<br/>
First turn on “Enable followup” and click save then turn on “Enable followups via email” and click save.<br/>
Select the “Email Followups Configuration”.<br/>
<img src="https://i.imgur.com/PVDpmIJ.png" height="60%" width="60%"/>
<br />
<br />
Fill in the information.<br/>
<img src="https://i.imgur.com/kjI47AI.png" height="60%" width="60%"/>
<br />
<br />
To find the SMTP Password. Click on “Manage your Google Account” and search for App passwords. You need to have 2-Step Verification enable to use App passwords.<br/>
Enter a name for the app, click create and copy the password, then click done.<br/>
<img src="https://i.imgur.com/h2PCQPi.png" height="60%" width="60%"/>
<br />
<br />
Once all the information is entered, click save then select “Send a test email to the administrator”.<br/>
Check if the test email was received.<br/>
<img src="https://i.imgur.com/eDz7y9X.png" height="60%" width="60%"/>
<br />
<br />
Back to GLPI. Click on the Setup option and select Automatic actions.<br/>
Select “queuednotification” and change the Run Mode from GLPI to CLI then click save.<br/>
<img src="https://i.imgur.com/mljJ3Ho.png" height="60%" width="60%"/>
<br />
<br />
Open Task Scheduler and select the Create Task option.<br/>
Enter a name, select “Run whether user is logged on or not” and check the “Run with highest privileges” box.<br/>
<img src="https://i.imgur.com/feqgsQq.png" height="60%" width="60%"/>
<br />
<br />
Select the Trigger option at the top, click new and configure the settings as shown below.<br/>
<img src="https://i.imgur.com/CXPE5Av.png" height="60%" width="60%"/>
<br />
<br />
Select the Action option at the top, click new and configure the settings as shown below. The php8.3.14 path will vary depending on the version being used.<br/>
<img src="https://i.imgur.com/RPT29nf.png" height="60%" width="60%"/>
<br />
<br />
Select the Setting option at the top and configure the settings as shown below. Once that is done click ok.<br/>
<img src="https://i.imgur.com/bVCa4Pi.png" height="60%" width="60%"/>
<br />
<br />
Right click the task and select run.<br/>
<img src="https://i.imgur.com/3tVhDBV.png" height="60%" width="60%"/>
<br />
<br />
Let’s create a ticket to see if we will receive an email.<br/>
<img src="https://i.imgur.com/sTRoRuP.png" height="60%" width="60%"/>
<br />
<br />
Let’s check our email.<br/>
<img src="https://i.imgur.com/vsew5ro.png" height="60%" width="60%"/>
<br />
<br />
</p>
