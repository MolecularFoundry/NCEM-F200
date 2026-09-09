## Saving in TEM Center
- Data is saved in S:, which is a mapped drive. The drive is physically located on the F200-support PC.
- TEM Center Data is converted to Tiff files

## Saving in GMS
- Data is saved in S:, which is a mapped drive. The drive is physically located on the F200-support PC.

## Saving in FEMTUS

## Saving in TVIPS\Dectris

## Saving in JED

## Saving Data to Crucible


## Accessing the Support PC from Windows PC (slow, ~ 0.1GB per minute)
- The support PC is connected to LBL network. 
- You should be able to log into the data drive using windows explorer and typing in \\\f200-support.dhcp.lbl.gov into the address bar.
- Use the login credentials for NCEMuser 
- You can then copy the data over to a local drive for analysis. 

## Accessing the Support PC from MacOS (slow, ~ 0.1GB per minute)
- The support PC is connected to LBL network. 
- You should be able to log into the data drive by connecting to a server (command+K) . Type in "f200-support.dhcp.lbl.gov" into the address bar, which will autocomplete to "smb://f200-support.dhcp.lbl.gov".
- Use the login credentials for NCEMuser 
- You can then copy the data over to a local drive for analysis. 

## Accessing the TVIPS PC from Windows PC (slow, ~ 0.1GB per minute)
- The TVIPS PC is connected to LBL network. 
- You should be able to log into the data drive using windows explorer and typing in \\\tvips-scan.dhcp.lbl.gov into the address bar.
- Use the login credentials with username "tvips", and password as indicated during training.  
- You can then copy the data over to a local drive for analysis. 

## Accessing the Support PC through Globus DTN (fast)
If your data is moved into the support computer data drive, you can access it remotely via globus.org . 
1. Navigate in a browser to globus.org
2. Click “Log In” in the upper right.
3. Select or search for your institution (most likely, LBL LDAP).
It is suggested that you use your home institution, your LBL, or NERSC account
You may have multiple logins combined into a single Globus account. Choose one as your main account
4. The File Manager tab should be open. Click on the Search box next to Collection at the top.For data at NCEM search for “NCEM JEOL F200”
5. You should be able to access files in your folder. 
6. To transfer between endpoints (NERSC → NCEM for example):
   1. In the upper right click on the side-by-side panel button
   2. Find the source and target endpoints in the two search boxes 
   3. Click on a file or set of files in only one panel 
   4. Click Start to start the transfer
Note: if start is grayed out make sure files are selected in only one side
Note: if you do not have access to your data, speak with someone at NCEM staff
7. For transfers of large amounts of data (size or number of files) please use Globus Connect Personal. Single files can be downloaded using the Download button  when a file is selected in the File Manager. 



