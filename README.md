# DiscountEngineToDatabase
Csv Directory Listener
This is a Scala project designed to listen to the files in a specified directory, process the contents of any CSV files, and store the results in a database. This project is built using Scala version 2.13.6, and it requires Java 1.8 or later to run.

Getting Started
To get started with this project, you will need to have Scala and Java installed on your machine. Then, follow these steps:

Clone this repository to your local machine
Open the project in your preferred Scala IDE or editor
Run the Main object to start the listener
Move your CSV files to the specified directory to begin processing
How it Works
This project uses the Java NIO file system library to monitor a specified directory for new files. When a new CSV file is detected, the program reads the contents of the file, processes the data according to a set of rules, and stores the results in a database.

The program uses a CsvDirectoryListener class to implement the file monitoring functionality. The class creates a WatchService to monitor the specified directory for new files, and it uses a Future to process each file asynchronously.

The calculateThePrice function applies a set of rules to the input data and calculates a final price for each row of data. The avg_Discount function applies various discount rules to a list of strings and returns a floating-point value representing the average discount percentage.

The program uses the JDBC API to connect to a PostgreSQL database and insert the processed data. The database connection details are specified in the config.properties file.

The program also writes a log file (logs.log) that contains information about the processing of each CSV file.

Configuration
The program uses a config.properties file to store the database connection details. You should update this file with the correct values for your database.

Dependencies
This project depends on the following libraries:

postgresql version 42.3.0
Java NIO file system version 2.13.6
These dependencies are managed using sbt.
