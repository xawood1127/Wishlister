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
