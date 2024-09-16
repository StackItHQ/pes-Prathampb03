# Google-sheets-mysql-connector

This is an application that connects google sheets with mysql such that any changes made in the google sheet is automatically reflected in the mysql table.
The google sheet used for the above application is https://docs.google.com/spreadsheets/d/1Mst2KT8HU4bsWw9-XEiW2QLgQJlNEu3YVUTk6G67UYU/edit?usp=sharing
All the changes are made to a mysql table  called student. 
The operations that are automatically updated in the sql table are  = insert,delete and update.
The code for the sql table has been added in the sql file . 
Planned Out Approach:
+--------------------+       +--------------------+       +----------------------+
|  Google Sheets     | ----> | Google Sheets API   | ----> | MySQL Database        |
|  (Insert/Update/   |       |  (Webhook or API    |       |  (Insert/Update/      |
|   Delete Rows)     |       |   call on changes)  |       |   Delete )            |
+--------------------+       +--------------------+       +----------------------+
            ^                                                |
            |                                                |
            +------------------------------------------------+
                    Track Google Sheets changes
