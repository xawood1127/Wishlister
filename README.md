# **WISHLISTER INSTALLATION INSTRUCTIONS**
#### To begin the installation process of our website please follow the instructions below to download the needed dependencies for the server:

### Installing NodeJS:

https://nodejs.org/en/download/current

●	Click the link above and select an installer appropriate to your operating system.

●	On completion of the download, run the installation file and follow the instructions to install NodeJS on your system. Whenever prompted with options, use the default option available.

●	After installation, open your command prompt by typing “cmd” in the Windows search bar.

●	In the command prompt window, type “node -v” and if a version number is returned, NodeJS was successfully installed on your system. 

●	If not, try uninstalling and installing the program again.

### Installing The System:

https://github.com/xawood1127/Wishlister

●	Go to the <>Code page

●	Download the file named “Wishlister.zip” under the main branch.

●	Once downloaded, go to your download location and extract the file to the location of your choice. After clicking extract, the default path will include the folder name but please remove it to look like this example pathway:
    Default: C:\Users\username\Downloads\Wishlister 
    Correct: C:\Users\username\Downloads\
    
●	After extraction, the system is ready to go. The next step to start the server for the website is to open the folder in a terminal:
    o	Windows 10: Shift + right-click on the Wishlister folder and click “Open Powershell Window Here”.
    o	Windows 11: Right-click on the Wishlister folder and click “Open in Windows Terminal”.
    
●	Once there, the file path should be the same as where the Wishlister folder is located. To run the server, type “node server.js”. Two prompts should appear, “Server started on 3000” and “MySQL Connected...”. This means your local server has successfully started!

●	The last step is to open your browser and go to http://localhost:3000/.

●	Once you are done with the site, you can close the server by typing CTRL + C in the command prompt or closing the command prompt window.

### For Future Developers, Installing the Database: 

https://dev.mysql.com/downloads/installer/ 

●	Keep the default options and download the “mysql-installer-community-8.0.36.0.msi”. 

●	Once downloaded, run the installer and all the MySQL tools will be installed on your system. For any prompts, keep the default options and continue to hit the “Next” button. When prompted to enter a password, enter any password you would like but make sure to note it as it is used to access the database. 

●	After installation, navigate to the MySQL command client and enter the following commands in sequential order: 

CREATE SCHEMA `wishlister`; 

CREATE TABLE `wishlister`.`users` ( 

  	`userId` INT NOT NULL AUTO_INCREMENT, 

  	`username` VARCHAR(255) NOT NULL, 

  	`email` VARCHAR(255) NOT NULL, 

  	`password` VARCHAR(255) NOT NULL, 

  	`profPic` VARCHAR(255) NOT NULL, 

  	`securQuest` VARCHAR(100) NOT NULL, 

  	`securAns` VARCHAR(255) NOT NULL, 

  	PRIMARY KEY (`userId`, `username`, `email`)); 

CREATE TABLE `wishlister`.`userlists` ( 

  	`id` int NOT NULL, 

  	`listId` int NOT NULL AUTO_INCREMENT, 

  	`listName` varchar(255) NOT NULL, 

  	`listItems` varchar(8000) NOT NULL, 

  	`itemPrices` text NOT NULL, 

  	`purchased` text NOT NULL, 

  	PRIMARY KEY (`listId`), 

  	KEY `id_idx` (`id`), 

  	CONSTRAINT `id` FOREIGN KEY (`id`) REFERENCES `users` (`userId`) ON 	DELETE RESTRICT ON UPDATE CASCADE) 

●	This should create the necessary tables in MySQL to allow you access to your own database. 

●	Now in the server.js file of the Wishlister.zip, the credentials at line 11 must be changed, replace all the code within the “mysql.createConnection({“ with the following: 

host: 'localhost', 

    		user: 'root', 

   		password: 'your password',	<- this is your password from earlier 

    		database: 'wishlister' 

●	Next delete line 9 and 2. You can also delete the “DigiCertGlobalRootCA.crt.pem” file from the Wishlister folder. 

●	Now you have access to maintain and edit your own database. 
