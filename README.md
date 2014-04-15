<<<<<<< HEAD
AWS-S3-Backup
=============

This is a simple Java client that allows the user to upload files to Amazon's S3. 


Setup Files
-----------

The process employs two files saved locally:

(1) "awskeys.json" which holds your AWS Access ID and Secret Key in the following format:

{"AWSKey1": ["AWS Access ID goes here"], "AWSKey2": ["AWS Secret Key goes here"]}

(2) "s3files.xml" which holds the files/folders that need to be backed up to S3. A model s3files.xml is provided in the src folder.

The <file> tag in s3files can hold file or folder names. 


(3) InitialSetup.java will create the two setup files. Before calling InitialSetup.java make sure to change the values in the main method to reflect your AWS Access ID, AWS Secret Key and path to files/folders that you would want to upload to S3. 

You may choose to create/populate the setup files through another method of your choice.

Backup Process
--------------

(1) Once the two setup files are created, start the backup process by calling BackupMain (java BackupMain).

(2) All the files/folders listed in your s3files.xml will be uploaded to S3 against relevant bucket names mentioned in s3files.xml.

(3) If a specified bucket is not present in your S3 account, it will be created before uploading the files.

Maven Build
-----------

(1) Use the provided pom.xml to build the project.

(2) A jar file named "AWS-S3-Backup-1.0.jar" will be created in the target folder.

(3) Create the two setup files as explained above. The files (awskeys.json, s3files.xml) will be created in the target folder.

(4) Start the backup process as: java -jar AWS-S3-Backup-1.0.jar





=======
JAX-WS-Client
=============

A JAX-WS client with SSL for the IBM System i/iSeries to connect to a web service through a proxy. 

Using the WSDL, create standard client stubs.

Add BDClient.java as a wrapper around the calling iSeries program (RPG or CL). It can be instantiated and called from the iSeries. It will perform necessary data conversions both ways - received from the iSeries and returned to the iSeries. 
BDClient.java retrieves SSL parameters from a Java Properties file.

The file BDProxy.java will make the call to the remote service. This file will be part of the created stubs. It is included here just to show the additional code customizations that need to be done. Parameters required for accessing the web service are stored in a configuration file. 
>>>>>>> 50da44d6c249cc1db4a4b84e3131f2c04376ad57


