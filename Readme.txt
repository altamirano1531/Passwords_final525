ADDENDUM II (May 2025)

The Password_final525 folder was created to incoprporate Added the capability to open a web browser with the selected web site defined in the website field entry_3 under the SITE INFORMATION. This functionality is  enabled by using the web button

Added delete question for users to verify the delete action.

Verified all websites and eleiminated a few sites not required anymore.

ADDENDUM (May 2025)

The Password_search folder was created to incoprporate the list search and autofill funtionality into the password application.

The application HI was also modified to include the SEARCH SITES, SITE LIST and SITE INFORMATION areas to delineate different functionality. When searching for site, the SEARCH SITES and SITE LIST work together to find specific sites according to the letters entered in the SEARCH SITES field and autofilling the SITES LIST list. NOTE that taking this action will disable the SITE EDITING buttons.
Once the site is found and it is clicked in the SITES LIST, the SITES INFORMATION fields will be filled with the site information. By clicking or focusing on the SITES INFORMATION fields the SITE EDITING buttons are enabled for use.

The application will run as before if the SEARCH SITES field is not used and selecting a site is done through the SITE LIST directly. Erasing all characters from the SEARCH SITES field will return the application to the original SITES LIST and previous operation mode.

The Passwords application (psswd.py) and distribution file creation software was uploaded to Github from C:\Workarea\Python\Passwords_2\Passwords_search. The Psswd.exe file was created with auto-py-to-exe and distribution file Passwords_setup.exe with Inno as described below.


### Create the distribution file by using psswd.py then create with auto-py-to-exe the psswd.exe. Finally create the distribution package with Inno tool Passwords_setup.exe


### Create the psswd.exe file with auto-py-to-exe ###
#####################################################
Perfrom the following command:
C:\Workarea\Python\Passwords_2\Passwords_final525> auto-py-to-exe
This opens the hi and then enter
Sript location:C:/Workarea/Python/Passwords_2/Passwords_final525/Psswd.py
Onefile: One Directory
Console Window:Windows based (hide the console)
Icon: N/A
Additional Files:
C:/Workarea/Python/Passwords_2/Passwords_final525/password.enc
C:/Workarea/Python/Passwords_2/Passwords_final525/key.key
C:/Workarea/Python/Passwords_2/Passwords_final525/information.json
Advanced:N/A
Settings:N/A

DO NOT use the onefile option under the Onefile selection instead use the One Directory option.

This is the prefered method to create the Psswd.exe. This method uses the PyInstaller but also correct many issues with the PyInstaller plus there is a human interface to ease use of the PyInstaller commands.



### Create the distribution file with Inno ###
##############################################

Create a Psswd.exe with auto-py-to-exe as shown above and copy the psswd.exe and _internal folder into the \Inno folder.

Go to the windows start and type Inno, then select Inno Setup Compiler.

After the Inno Setup compiler opens in the welcome screen select Create a new script file using the Script Wizard.

NEW SCRIPT
Sript Wizard Welcome: Next
Application Information - Name: Passwords - then Next
Application Folder - Next
Application Files 
-Application Main executable..:C:\Workarea\Python\Passwords_2\Passwords_final525\Inno\Psswd.exe
-Other applications files: 
-- Add Folder: C:\Workarea\Python\Passwords_2\Passwords_final525\Inno (Answer Yes to add all files under the folder)
Application File Association N/A - Next
Application Shortcuts ... N/A - Next
Application Documentation ... N/A - Next
Setup Install Mode - Non Administrative Install Mode - Next
Application Registry Keys ... N/A - Next
Setup Languages ... N/A - Next
Compiler Settings 
- Custom Compiler output folder: C:\Workarea\Python\Passwords_2\Passwords_final525\Inno
- Compiler output base file name: Passwords_setup - Next
Inno Setup Preprocessor - Next
Finish - Next

Compile the new sript - Yes
Would you like to save script before compiling - Yes
File Name:Passwords_script - Save

Now go to the \Inno folder and run Passwords_setup.exe

Select destination Location - Accept C:\Users\Arturo\AppData\Local\Programs\Passwords_final525
Additional tasks - Create a desktop shortcut
Ready to Install - Install
Finish.

The \Inno\Passwords_setup.exe can now be used to distribute it and install the Psswd.exe with supporting files for use.

### END