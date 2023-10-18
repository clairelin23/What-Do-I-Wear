# What Do I Wear?

This repo contains the project developed by Team 21 ([Devin Gonzales](https://github.com/DJGonzales96), [Claire Lin](https://github.com/clairelin23), and [Patrick Silvestre](https://github.com/pjsilvestre)) for CS 157A at San Jose State University during the Fall 2019 semester.

## Project Documentation

[Project Proposal](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Proposal.md)

[Project Requirements](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Requirements.md)

[Project Data Model and Database Design v1](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Data_Model_And_Database%20Designs/Project_Data_Model_and_Database_Design_v1.md)

[Project Data Model and Database Design v2](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Data_Model_And_Database%20Designs/Project_Data_Model_and_Database_Design_v2.md)

[Project Data Model and Database Design v3 (Current)](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Data_Model_And_Database%20Designs/Project_Data_Model_and_Database_Design_v3.md)

[Project Final Report](https://github.com/pjsilvestre/CS157A-21/blob/master/docs/Project_Final_Report.md)

## Running in Development Mode

### Downloading the App

Run the following using your shell:

```sh
git git@github.com:pjsilvestre/CS157A-21.git
cd CS157A-21/express-app
```

### Setting up MySQL

Make sure you have [MySQL](https://www.mysql.com/) installed, and start your server using your shell:

```sh
sudo mysql.server start
```

If your MySQL root password is not `password`, you can change it as follows using your shell, then MySQL:

```sh
$ mysql -u root -h localhost -p
Enter your password: ****************
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';
```

Alternatively, navigate to `express-app/config/database.js`, and change authentication details as necessary.

### Populating the Database

Run the following using MySQL, replacing `<...>` with the directory containing `CS157A-21`:

```sh
mysql> source <...>/CS157A-21/sql/initialize-schema-and-data.sql
```

### Running the App

Make sure you have [Node.js](nodejs.org) installed, then run the following using your shell, making sure you're in the `CS157A-21/express-app` directory:

```sh
npm install
npm run devstart
```

The app should now be running on [localhost:3000](localhost:3000).
