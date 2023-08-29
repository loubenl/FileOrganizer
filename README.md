# FileOrganizer

**Summary**
- Files from user-provided paths are collected and stored in a database along with thier attributes (file size, date created, type)
- User needs to give directory to where to create the new directories
- Create new directories for each file type and organizes the files in the directories accordingly.
- Provide analysis : for each category, give the avg size of storage used, give how many items
- File management manipulation features available *more details below*

**Features**
- Command line argument given "-backup" backups these files in a database?
- From cin, argument "display-info" to print table of the details from the database 
  
Management of Documents:
- Predefined queries available for user-provided directory (eg past 5 hours, 1 day, 5 days, week, month, 6 months)
- Sort files in user-provided directory alphabetically
- Sort files in user-provided directory by time
- command line argument to copy or move the files



Download PostGresSQL. 

User Should give the full path names of the directory to UI. 

Better to first put all info in databse as is, yes.

 Process for Scanning (automatically): 
 - scan system (scan + update)
 - Set flags in database to false
 - In loop:
 - find path
 - convert to hash value
 - compare this hash value in databases. New Record, Update Record, Delete Record.
1. If the hash values match each other, you make update in database and set the flag of the file to true 
2. If not, you create new record and set the flag of the file to true
(adding: size, path name, hash table, cross reference with map of extensions and the document type and add the document type to the database)
For each file, you have a full path. Based on this path, you create a hash value.
- Go through all flags that are false and delete them
Show file scanning detail (aka in progress) :
"Scanning in progress"
"Finished Scanning"


- ability to run queries and run reports

  
