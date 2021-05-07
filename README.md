# https-github.com-openmrs-openmrs-module-fdah

OPEN MRS steps

1. Download Maven 3.6.3, Eclipse 4.16.0, SQL
2. Go to GitHub https://github.com/openmrs/openmrs-core and fork the repository 
3. Download onto your git desktop 
4. Download SDK using these steps https://wiki.openmrs.org/display/docs/OpenMRS+SDK#OpenMRSSDK-Installation
    1. press enter for db name and user name
5.  Open Eclipse IDE
6. Click Help -> Install New Software...
7. Click Add button at top right corner
8. At pop up: fill up Name as "M2Eclipse" and Location as "http://download.eclipse.org/technology/m2e/releases" 
9. Accept the agreement & click finish.
10. Under maven folder click existing  maven projects
11. Locate git folder
12. Right click on the openmrs file in the project
13.  Click on run as Maven Build
14.  In the name section type "openmrs-core clean test install"
15.  In the goal section type "clean install"
16. Click run 
17.  Right click on the openmrs-webapp 
18.  Click on Debug as Maven Build 
19.  In the name section type "openmrs-webapp jetty"
20.  In the goal section type "jetty:run"
21. Click on the JRE tab we need to allocate memory 
22. Under VM arguments type "-Xms1024m -Xmx2048m -XX:PermSize=512m”
23. Click debug 
24. Intall SQL (error I had was mysql can't be installed a new vierson of this software already exists on this disk, so if you previously had SQL installed you need to go to system preferences, mysql and uninstall it from there) https://downloads.mysql.com/archives/community/ 
25. https://www.youtube.com/watch?v=UcpHkYfWarM&t=257s
26. Go to system preferences and mySQL pane will be available
27. Start mySQL server
28. Set root password for mysql- Open terminal
29. Type:  cd /usr/local/mysql
30. Type: cd bin
31. Type:  ./mysqladmin --u root password '(type password here)'  note need to remember password.
32. Download mySQL workbench https://downloads.mysql.com/archives/workbench/
33. Open mySQL workbench and create local connection with password (for troubleshooting https://stackoverflow.com/a/36252036)
34. Connect SQL to mySQL 
35. Type in command line: mkdir /usr/local/etc/my.cnf.d
36. Type in command line: sudo /usr/local/mysql/support-files/mysqld_multi.server start
37. Open a browser and type http://localhost:8080/openmrs/index.htm​l
38.  Click on simple, enter password for computer, next. You will see a tasks to execute page
39. Go to eclipse, the server will start running 
40. start server mvn openmrs-sdk:run
