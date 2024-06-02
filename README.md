# Digital Forensic Example Case #
Fraud Case With USB Drive Image

Steps:
Download Fraud Image : 
https://drive.google.com/file/d/1Cqw3gcExVAecIQx3jY7VNetkcLeJO9x8/view?usp=sharing

Mount From Kali Linux:
# mkdir evidence
# mount -o loop fraud.img evidence

Check File List 
# cd evidence
# ls -al
(explore using file manager)

Check File Type
# file locked.jpeg
# file password.jpeg

Check Back The Image File
# cd ..
# fls fraud.img

Check Deleted Files:
# fls -r fraud.img

Check Inodes Status:
# istat fraud.img 11 

Recover The File
#icat fraud.img 11 > readme.txt

Search For Passwords
# srch_strings -a -t d fraud.img > fraud.str
# grep password fraud.str