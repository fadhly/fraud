# Digital Forensic Example Case #
Fraud Case With USB Drive Image

Steps:
Download Fraud Image : 
https://drive.google.com/file/d/1Cqw3gcExVAecIQx3jY7VNetkcLeJO9x8/view?usp=sharing

Mount From Kali Linux:
# mkdir evidence
# sudo mount -o loop fraud.img evidence

Check File List 
# cd evidence
# ls -al
(explore using file manager)

Check File Type
# file locked.jpeg
# file password.gif

Check Back The Image File
# cd ..
# fls fraud.img

Check Deleted Files:
# fls -r fraud.img

Check Inodes Status:
# istat fraud.img 11 
# istat fraud.img 12
# istat fraud.img 13 

Recover The File
# icat fraud.img 11 > readme.txt
# icat fraud.img 12 > Secret.doc
# icat fraud.img 13 > Shower.avi

Check File Type
# file readme.txt
# file Secret.doc
# file Shower.exe

Search For Passwords
# srch_strings locked.jpeg | grep password > password1.txt
# srch_strings password.gif | grep password > password2.txt