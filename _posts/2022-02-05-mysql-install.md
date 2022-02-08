---
title: "MYSQL Installation Guide"
tags: [MySQL, Installation, Databases]
style: 
color:
description: MySQL is a developer-friendly open source relational database management system. Reliable and easily scalable, MySQL powers the back end of many popular social, streaming, and service web applications.
---
Author: [Ajay Srivastava](https://ajaydevelopr.github.io/)

To install MySQL on your machine, follow the instructions provided for your operating system.

#### Install MySQL Server on Windows
* To install the MySQL server on a Windows computer, visit the [MySQL Community Downloads page](https://dev.mysql.com/downloads/mysql). In the Select Operating System dropdown menu, choose Microsoft Windows, as shown in the following image:
![](https://i.ibb.co/SnTtkpR/12-sql-mysql-win-demo-00.png)

* Next to "Windows (x86, 32 & 64-bit), MySQL Installer MSI", select "Go to Download Page". On the next page, find the "Windows (x86, 32-bit), MSI Installer" option that is the smaller file size, and click the Download button. This should look like the following image:
![](https://i.ibb.co/Xyky9nj/12-sql-mysql-win-demo-01.png)

* When prompted about signing up for a free Oracle Web account on the next page, select "No thanks, just start my download," as shown in the following image:
![](https://i.ibb.co/ZcNq8Fk/12-sql-mysql-win-demo-02.png)

* Navigate to the folder where the file was downloaded, and double-click it to run the installer. If you get prompted for an update, select Yes. When you reach the page labeled "Choosing a Setup Type", check that "Server only" is selected, and click Next:
![](https://i.ibb.co/KxmgKmt/12-sql-mysql-win-demo-03.png)

* On the next screen, entitled Download, you'll see your product listed (it should say "MySQL Server" followed by a version number). Click Execute to start the installation process, as shown in the following image:
![](https://i.ibb.co/hcfNhY5/12-sql-mysql-win-demo-04.png)

* After you click Execute, the status will be listed as Downloaded. Click Next, as shown in the following image:
![](https://i.ibb.co/HCWwVZK/12-sql-mysql-win-demo-05.png)

* The MySQL server is now ready for installation. Click Execute to begin the installation, as shown in the following image:
![](https://i.ibb.co/hH9HcLg/12-sql-mysql-win-demo-06.png)

* Once the installation status shows as Complete, click Next, as shown in the following image:
![](https://i.ibb.co/n6KmDJ4/12-sql-mysql-win-demo-07.png)

* Then click Finish on the next page, which should indicate Installation Complete, as shown in the following image:
![](https://i.ibb.co/pwwZkVX/12-sql-mysql-win-demo-08.png)

* At this point, the installer should close on its own. Reopen it and click on the Reconfigure link under Quick Action, as shown in the following image:
![](https://i.ibb.co/SvxgfkV/12-sql-mysql-win-demo-09.png)

* On the Type and Networking screen, don't change anything, and click Next.
  * Important On the Authentication Method screen, select "Use Legacy Authentication Method (Retain MySQL 5.x Compatibility)" and click Next, as shown in the following image:
  ![](https://i.ibb.co/44cG7s9/12-sql-mysql-win-demo-10.png)

  * On the next screen, Accounts and Roles, you'll need to enter a strong password under Root Account Password, near the top of the screen. Make sure to enter a unique password that you've never used before. Then repeat your root password in the next field, as shown in the following image:
  ![](https://i.ibb.co/SvSKjK7/12-sql-mysql-win-demo-11.png)

  * Caution Don't forget your password! It's extremely important that you keep track of your root password for MySQL, as it's difficult to reset. Write it down somewhere easily accessible, or add it to a password manager to keep it secure.

* After entering your password twice and ensuring that you've stored it somewhere you can find it, click Next.

* On the next screen, Windows Service, don't change anything, and click Next. On the Apply Configuration screen, click Execute to apply the changes, as shown in the following image:
![](https://i.ibb.co/PNWQDXF/12-sql-mysql-win-demo-12.png)

* After the configuration is complete, click Finish.
  > Note If you have any issues with the Windows (x86, 32-bit), MSI Installer that is the SMALLER file size, go back and download the LARGER size, following the same steps.

Now you'll need to add the PATH to the MySQL install to your environmental variables.

#### Add the MySQL PATH to Environmental Variables
* First you'll need to copy the PATH to MySQL to your clipboard. Open any folder on your computer and select This PC in the left-hand navigation bar, as shown in the following image:
![](https://i.ibb.co/WWz5y0w/12-sql-mysql-win-demo-13.png)

* Next, double-click your C: drive, as shown in the following image:
![](https://i.ibb.co/gPbv5Ff/12-sql-mysql-win-demo-14.png)

* Double-click the Program files folder, then double-click the MySQL folder.
  > Note Depending on the version of Windows on your computer, MySQL might be inside the ```Program files (x86)``` folder.

* Double-click the MySQL Server 8.0 folder, and finally, double-click the bin folder. Your screen should look like the following image:
![](https://i.ibb.co/BqLvj5h/12-sql-mysql-win-demo-15.png)

* Right-click the address at the top of the screen and select "Copy address as text", like in the following image:
![](https://i.ibb.co/41V2yFT/12-sql-mysql-win-demo-16.png)

* Now that you've got the PATH copied to your clipboard, press the Windows key on your keyboard and search for "Edit the system environment variables". Once that appears in the search screen, click on it, as shown in the following image:
![](https://i.ibb.co/vBKVYkY/12-sql-mysql-win-demo-17.png)

* You'll then be prompted with the System Properties screen. Navigate into the Advanced tab and select "Environment Variables...", as shown in the following image:
![](https://i.ibb.co/BgVdX6n/12-sql-mysql-win-demo-18.png)

* On the Environment Variables screen, under "User variables for <user>" (where <user> is your username on that computer), click into Path and then click the "Edit..." button in the top section of the screen. It should look like the following image:
![](https://i.ibb.co/kMCY24J/12-sql-mysql-win-demo-19.png)

* In the "Edit environment variable" window, select New, as shown in the following image:
![](https://i.ibb.co/dQXC8Kt/12-sql-mysql-win-demo-20.png)

* Your cursor will appear in a new line at the bottom of the variables. Paste your PATH in this box and click OK. Your screen should resemble the following image:
![](https://i.ibb.co/Pr4SSN1/12-sql-mysql-win-demo-21.png)

* Once you've added the PATH, restart Git Bash completely. You can verify that the installation was correct by typing the following into Git Bash:
```Git
mysql -V
```
* The PATH followed by the MySQL version number should be printed to the screen. Once you verify that the MySQL server was correctly installed, you can move on to setting up MySQL Shell.

#### MySQL Shell on Windows
  > Important To use MySQL commands, you'll need to use MySQL Shell. You won't be able to access this shell through your Git Bash terminal—you'll need to use the Windows command prompt.

* To open MySQL Shell, press the Windows key and the R key at the same time. This will bring up a dialog window titled Run. Enter "cmd" in the input and click OK, as shown in the following image:
![](https://i.ibb.co/LZnPpch/12-sql-shell-demo-01.png)

* This will open your Windows command prompt, which will look something like the following image:
![](https://i.ibb.co/YZQwkj1/12-sql-shell-demo-02.png)

* From here, you'll be able to use the cd command to navigate to the directory where you're working. The following command, for example, will move you into the directory of a sample folder:
```Git
cd Desktop/sample-folder
```
You'll see something like the following image:
![](https://i.ibb.co/5Gx34N3/12-sql-shell-demo-06.png)

* Once you're there, you'll need to log into MySQL Shell. To do so, enter the following command in the Windows command prompt:
```Git
mysql -u root -p
```

* This tells MySQL Shell that you want to log in with the root user (-u). The -p syntax stands for "password." Once you enter this command, you'll be prompted for the root password that you created when you installed MySQL, as shown in the following image:
![](https://i.ibb.co/4Wn7rfM/12-sql-shell-demo-07.png)

* Enter your password and press the Enter key. This will log you into MySQL Shell, as shown in the following image:
![](https://i.ibb.co/kgjJsyV/12-sql-shell-demo-08.png)

* From here, you'll be able to enter MySQL commands. You don't need to do this now, but you can revisit these instructions as you work through this module.

Type the command quit; to exit MySQL Shell.
  * Deep Dive You can also access MySQL Shell directly in VS Code! Depending on how you set up Git Bash, this option might already be available to you. Select Terminal from your menu at the top of the screen, and select New Terminal in the dropdown menu, as shown in the following image:
  ![](https://i.ibb.co/kHbqrkp/12-sql-shell-demo-04.png)

  * If a terminal appears at the bottom of your screen with "cmd", "powershell", or "bash" selected, you're ready to go. You can click on this dropdown to choose the integrated terminal of your choice. See the following image for an example:
  ![](https://i.ibb.co/pLnCTNX/12-sql-shell-demo-05.png)
  If you can't access an integrated terminal and you want to, see the VS Code documentation on the integrated terminal.