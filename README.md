<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This section will demonstrate the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Demonstration</h2>

 - ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=K7T_JjvEamg)

<h2>Environments and Technologies Used</h2>

 -  Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

 -  Windows 10

<h2>Installation Steps</h2>

<h2>Step 1: Download the Files</h2>

<img src="https://github.com/kwakuayimkorankye/osticket-prereqs/blob/main/ostick1.PNG" height="80%" width="80%" alt="Download Page"/>

<p>To get started you first will download <a href="https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0">this link</a> to install the necessary files to install osTicket</p>

<h2>Step 3: Download the Files</h2>

<ol>
  <li>Download <b>osTicket-Installation-Files.zip</b>.</li>
  <li>Extract it to your Desktop.</li>
</ol>

<hr>

<h2>Step 2: Turn On IIS</h2>
<img src="https://github.com/kwakuayimkorankye/osticket-prereqs/blob/main/ostick2.PNG" height="80%" width="80%" alt="IIS"/>
<p>Go to:</p>

<pre>
Control Panel
→ Programs
→ Turn Windows features on or off
</pre>

<p>Enable:</p>

<pre>
Internet Information Services
→ World Wide Web Services
→ Application Development Features
→ ✔ CGI
</pre>

<hr>

<h2>Step 3: Install the Programs</h2>

<p>Install these in order:</p>

<ol>
  <li>PHP Manager</li>
  <li>Rewrite Module</li>
  <li>Create <code>C:\PHP</code></li>
  <li>Extract PHP into <code>C:\PHP</code></li>
  <li>VC_redist.x86.exe</li>
  <li>MySQL 5.5.62</li>
</ol>

<p>When installing MySQL:</p>

<pre>
Username: root
Password: root
</pre>

<hr>

<h2>Step 4: Set Up PHP</h2>

<ul>
  <li>Open IIS as Administrator.</li>
  <li>Open PHP Manager.</li>
  <li>Select <code>C:\PHP\php-cgi.exe</code>.</li>
  <li>Restart IIS.</li>
</ul>

<hr>

<h2>Step 5: Install osTicket</h2>

<ol>
  <li>Extract <b>osTicket-v1.15.8.zip</b>.</li>
  <li>Copy the <b>upload</b> folder to:</li>
</ol>

<pre>
C:\inetpub\wwwroot
</pre>

<p>Rename <b>upload</b> to <b>osTicket</b>.</p>

<p>Restart IIS.</p>

<hr>

<h2>Step 6: Enable PHP Extensions</h2>

<p>In IIS → PHP Manager, enable:</p>

<ul>
  <li>php_imap.dll</li>
  <li>php_intl.dll</li>
  <li>php_opcache.dll</li>
</ul>

<p>Refresh the webpage.</p>

<hr>

<h2>Step 7: Configure osTicket</h2>
<img src="https://github.com/kwakuayimkorankye/osticket-prereqs/blob/main/ostick3.PNG" height="80%" width="80%" alt="osTIcket Loading Page"/>

<p>Rename:</p>
<img src="https://github.com/kwakuayimkorankye/osticket-prereqs/blob/main/ostick4.PNG" height="80%" width="80%" alt="Sample Confing"/>

<pre>
ost-sampleconfig.php
</pre>

<p>to</p>

<pre>
ost-config.php
</pre>

<p>Give <b>Everyone</b> Full Control.</p>

<hr>

<h2>Step 8: Create the Database</h2>

<ul>
  <li>Install HeidiSQL.</li>
  <li>Log in with:</li>
</ul>

<pre>
Username: root
Password: root
</pre>

<p>Create a database named:</p>

<pre>
osTicket
</pre>

<hr>

<h2>Step 9: Finish Setup</h2>

<p>Fill in:</p>

<ul>
  <li>Helpdesk Name: <b>Helpdesk</b></li>
  <li>Database: <b>osTicket</b></li>
  <li>Username: <b>root</b></li>
  <li>Password: <b>root</b></li>
</ul>

<p>Click <b>Install Now!</b></p>

<hr>

<h2>Step 10: Clean Up</h2>

<ul>
  <li>Delete the <code>setup</code> folder.</li>
  <li>Set <code>ost-config.php</code> to <b>Read Only</b>.</li>
</ul>

<hr>

<h2>✅ You're Done!</h2>

<p>Your admin page:</p>

<pre>http://localhost/osTicket/scp/login.php</pre>

<p>Your help desk page:</p>

<pre>http://localhost/osTicket/</pre>

<p><b>🎉 Congratulations! Your osTicket help desk is ready to use.</b></p>

<br />
