# AdvanceJava

Maven
  Required THings
        Internet
        <GroupId>        Project Name  which name is to give to jar file.
        <Artifact ID>    Minimum Required
        <version  >       Default 0.0.1
        
  Mother Repo
      www.mvnrepository.com
      
  arctype=arcitect Type.
      it provides some default templets.
      
  pom.xml   = project Object Model (kundali of Project)
  
steps
  1.Go to www.mvnrepository.com
  2.search mysql.
  3.click on mysql connector/J
  4.click on version 8.0.32
  5.and download the code behind it
    i.e.    <!-- https://mvnrepository.com/artifact/com.mysql/mysql-connector-j -->
            <dependency>
                <groupId>com.mysql</groupId>
                <artifactId>mysql-connector-j</artifactId>
                <version>8.0.32</version>
            </dependency>

                                                                                                      08/03/2023
   Todays Topics Discussed...
            
            To select the database use following command.
                      > use DataBase_Name;
                 
                                                                                                      09/03/2023
    
     Download and install the MySQL JDBC driver:
  
      You can download the MySQL JDBC driver from the official MySQL website: https://dev.mysql.com/downloads/connector/j/
      Extract the contents of the downloaded ZIP file to a folder on your computer.
      Load the MySQL JDBC driver:
  
      To load the MySQL JDBC driver, you need to use the Class.forName() method, as follows:
      vbnet
      Copy code
      Class.forName("com.mysql.cj.jdbc.Driver");
      Establish a database connection:
      To establish a connection to a MySQL database, you need to specify the URL of the database, username, and password.
      The URL should be in the format: jdbc:mysql://hostname:port/databasename
      java
      Copy code
      String url = "jdbc:mysql://localhost:3306/mydatabase";
      String username = "myusername";
      String password = "mypassword";
      Connection connection = DriverManager.getConnection(url, username, password);
      Execute SQL queries:
      Once you have established a database connection, you can execute SQL queries by creating a Statement object and calling its executeQuery() method.
      For example, to execute a simple SELECT query, you can use the following code:
      java
      Copy code
      Statement statement = connection.createStatement();
      ResultSet resultSet = statement.executeQuery("SELECT * FROM mytable");
      while (resultSet.next()) {
        // Process each row of the result set
      }
      Close the database connection:
        It is important to close the database connection when you are done using it, to release any resources associated with it.
        You can do this by calling the Connection object's close() method:
          go
          Copy code
          connection.close();
    Note: It is recommended to use try-with-resources statement to automatically close resources such as connection, statement and resultSet.
