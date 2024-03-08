<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Make sure to enable CGI before downloading anything
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>

<img src="https://i.imgur.com/dB5Oo2B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this very first step after opening your virtual machine you should enable CGI. What you have to do to enable CGI is go to start->programs and features->Internet Information Services->Application Features and then you should be able to find CGI and enable it.
</p>
<br />

<p>
<img src="https://i.imgur.com/Lzhc0oz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This second step is pretty important but it's not really one step because it's a whole bunch of other steps together. This picture is where I get everything i need to download from you will basically want to download all of these in the regular settings. You want to install everything here except for OSTICKET and HEIDI SQL. After downloading all the necessary downloads you want to make called "PHP" and then extract all "php-7.3.8-nts-Win32-VC15-86 to the PHP folder created. Open IIS as an admin and then open the PHP manager->register new PHP in PHP folder-> click PHP CGI and then restart the IIS server.
</p>
<br />

<p>
<img src="https://i.imgur.com/W6AbvdW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step i'm going to get you to open OSTICKET. Now is the time to install OSTICKET after installing this you will copy and extract the "upload" folder->windows C:->inetpub->wwwroot->rename upload to "os-ticket". Last step to get into OSTICKET is to go to IIS then click osticket vm->sites->default website->osticket-> then click browse.
</p>
<br />

<p>
<img src="https://i.imgur.com/owTtvPa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After this you should be able to see OSTICKET some things are unchecked we will change that. First thing we'll want to do is go to the PHP manager and enable "php.imap.dll", php-intl.dll and php-opcache.dll restart php servers as usual. Now it should be fixed and look like the picture. Visit wwwroot->osticket->upload->include->rename "ost-sample.php" to "ost-config.php". Now we will be giving everyone access to the file by right click "ost-config.php"->properties->security->disable their inheritance->principal->insert "everyone" then check name-> give full control.
</p>

<p>
<img src="https://i.imgur.com/MVrW2vB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This is pretty much the final step to actually logging into OSTICKET. Now is the time to download Heidi SQL since we need to get the database to login to OSTICKET but just login with any account information wanted. After downloading Heidi open it and create new->proceed to enter the username and password used for MYSQL->click open->right click to create new database called "OsTicket". Click install now after entering the database settings. OSTICKET should say "Congratulations" when finished. Last step is to change Os-Ticket folder permissions for everyone to read and execute because we only wanted you to have all the permissions so now you can change that since you're logged in.
</p>
<br />
