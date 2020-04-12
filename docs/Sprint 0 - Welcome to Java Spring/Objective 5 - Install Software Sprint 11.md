# Install Software Needed for this Sprint

* PostgreSQL
* Environment Variables

<details>
<summary>PostgreSQL</summary>

The homepage for PostgreSQL is [https://www.postgresql.org/](https://www.postgresql.org/)

<details>
<summary>PostgreSQL for Mac</summary>

![Video Lecture](assets/novideo.png)

* Before installing, close out of all programs except your browser. DO NOT use your computer during the installation process!
* Download the latest version of the EDB PostgreSQL Database for Mac OS X from
  [https://www.enterprisedb.com/downloads/postgres-postgresql-downloads](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)
  * Double click on dmg file that was just downloaded
  * We are going to install using the defaults suggested
  * Double click on the postgresql-XX.XX-osx file that appears
    * Agree to install it from the scary internet!
  * You may have enter your password to install
    * Click Next
    * Click Next
    * Click Next
    * Click Next
    * Enter a password. Keep it simple as you will need to remember it for the rest of the class. I suggest something like `password`.
    * Leave the port at the default of 5432
    * Keep clicking Next, taking the defaults until you get to the Installing screen.
    * Allow PostgreSQL to install.
    * Be patient. Installation may take awhile.
    * DO NOT USE COMPUTER WHILE INSTALLING.
      * PostgreSQL is a difficult enough installation.
      * Use of your computer during installation will cause issues.
    * Uncheck Launch Stack Builder. We will not need it for class.
    * Click Finish
    * Restart your computer before testing the installation.
  * This installs both the database management system PostgreSQL and the GUI access tool pgAdmin.
    * Launch the pgAdmin ![pgAmdin](assets/pgAdminIcon.png) tool
    * You will be prompted to set a master password. I would recommend something easy like `password`. You will need to remember this password as well.
  * PostgreSQL is now installed!


For more information, see [https://www.enterprisedb.com/postgres-tutorials/installation-postgresql-mac-os](https://www.enterprisedb.com/postgres-tutorials/installation-postgresql-mac-os)
</details>

<details>
<summary>PostgreSQL for Windows 10</summary>

![Video Lecture](assets/novideo.png)

* Before installing, close out of all programs except your browser. DO NOT use your computer during the installation process!
* Download the latest version of the EDB PostgreSQL Database for Windows x86-64 from
  [https://www.enterprisedb.com/downloads/postgres-postgresql-downloads](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)
  * You will need to run the file
    * This can either be done as an option prior to downloading
    * Or you can launch the file after downloading
  * Start installing, accepting the defaults
    * You will be prompted to create a password
      * YOU MUST REMEMBER THIS PASSWORD. IT IS NEEDED THROUGHOUT THE CLASS
      * I suggest something easy like `password`
    * Leave the PORT setting at the default of 5432
    * Accept the rest of the defaults and start installing
    * Be patient. Installation may take awhile.
    * DO NOT USE COMPUTER WHILE INSTALLING.
      * PostgreSQL is a difficult enough installation.
      * Use of your computer during installation will cause issues.
    * Uncheck Launch Stack Builder. We will not need it for class.
    * Click Finish
    * Restart your computer before testing the installation.
  * This installs both the database management system PostgreSQL and the GUI access tool pgAdmin.
    * Launch the pgAdmin ![pgAmdin](assets/pgAdminIcon.png) tool
    * You will be prompted to set a master password. I would recommend something easy like `password`. You will need to remember this password as well.
  * PostgreSQL is now installed!

For more information see [https://www.enterprisedb.com/edb-docs/d/edb-postgres-advanced-server/installation-getting-started/installation-guide-for-windows/12/EDB_Postgres_Advanced_Server_Installation_Guide_Windows.1.08.html](https://www.enterprisedb.com/edb-docs/d/edb-postgres-advanced-server/installation-getting-started/installation-guide-for-windows/12/EDB_Postgres_Advanced_Server_Installation_Guide_Windows.1.08.html)

</details>

<details>
<summary>PostgreSQL for Ubuntu</summary>

![Video Lecture](assets/novideo.png)

* From the terminal prompt, enter the following commands

```BASH
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
sudo apt-get install curl ca-certificates gnupg
curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install postgresql-12 pgadmin4
```

* now we need to set a password for our PostgreSQL database. From a terminal prompt enter

```BASH
sudo -u postgres psql postgres
```

* This will take to you a PostgreSQL prompt `postgres=#`
* At that prompt enter

```BASH
\password postgres
```

* You will be prompted to enter a new password. Pick something simple like `password`. You will need to remember it for the rest of the class and beyond!
* To exit from the postgres command line interface, type `exit`

* This installs both the database management system PostgreSQL and the GUI access tool pgAdmin.
  * Launch the pgAdmin ![pgAmdin](assets/pgAdminIcon.png) tool
  * You will be prompted to set a master password. I would recommend something easy like `password`. You will need to remember this password as well.

For more information see [https://wiki.postgresql.org/wiki/Apt](https://wiki.postgresql.org/wiki/Apt)
</details>

<details>
<summary>PostgreSQL in the Cloud (on Heroku)</summary>

![Video Lecture](assets/novideo.png)

If for some reason you cannot get PostgreSQL installed on your computer, all is not lost! For the class assignment on RDBMS you can use PostgresSQL on the Cloud system Heroku. Here is how.

This is also useful for when we deploy a PostgreSQL based application to Heroku and need to look at the database itself!

We must first setup an Heroku and install the Heroku CLI. You need this anyway so might as well do it now!

* See [Objective 6 - Install Software Sprint 12](Objective%206%20-%20Install%20Software%20Sprint%2012.md)
  * Heroku Cloud Account
  * Heroku CLI

Now we need to create a PostgreSQL instance on Heroku. Let's use the Heroku CLI to do this!

* From a command / terminal prompt

```BASH
heroku login
```

* Pressing a key will launch a web browse where you can sign in Heroku.
* Enter the username and password of your Heroku account and close out of the web browse.
* You are returned, signed in, to the command / terminal prompt.
  * You will get a message that you are `Logged in as <username>`
  * If you don't get this message, repeat the steps! This is a common issue with Heroku CLI.

* Once you are signed on, create a Heroku app.
* I like to name my apps < my user name > - < my application name >
  * my standard username is jrmmba
  * we are creating a PostgreSQL instance
  * so I will name my app jrmmba-postgresql
  * Note that all app names on Heroku must be unique!
* From a command / terminal prompt, substituting your app name for `jrmmba-postgresql`

```BASH
heroku create jrmmba-postgresql
```

* You will receive a prompt that tells you how you can access your Heroku app on the web. In my example this is `https://jrmmba-postgresql.herokuapp.com/`

* Now we need to add PostgreSQL to our app. Enter the following command from a command/terminal prompt

```BASH
heroku addons:create heroku-postgresql:hobby-dev -a jrmmba-postgresql
```

* Now we need to find some Heroku info such as username, database name, password, host. Enter the following command from a command/terminal prompt

```BASH
heroku config -a jrmmba-postgresql
```

* You will get a DATABASE_URL displayed. This URL contains the information that we need. Below is a sample URL. Underneath it is a layout of the URL. If you will copy your URL to a text file and then past the layout of the URL under it, reading the information will be much easier.

```TEXT
postgres://szpdsfwndvfcsb:759f951ea4289cabc53bb07128aa60675d2e17ee5e0f92a9d3e0020f831cff73@ec2-18-235-97-230.compute-1.amazonaws.com:5432/d2puqdoih80btl
posgress://username      :password                                                        @url host                                 :5432/dbname
```

* We need the
  * Username, the characters from the `//` to the second `:`
    * `szpdsfwndvfcsb`
  * Password, the characters from the second `:` to the `@`
    * `759f951ea4289cabc53bb07128aa60675d2e17ee5e0f92a9d3e0020f831cff73`
  * Host, the characters from the @ to the third `:`
    * `ec2-18-235-97-230.compute-1.amazonaws.com`
  * Database name, the characters from the last `/` to the end
    * `d2puqdoih80btl`

* Armed with this information, launch pgAdmin ![pgAdmin Icon](assets/pgAdminIcon.png)
  * This does assume you have tried to installed PostgreSQL for you operating system. Normally pgAdmin gets installed just fine; issues arise with the PostgreSQL database system. If that is not your experience, time to ask for help!!!

* You may be asked to create a master password or sign in using a master password you have already created. Again I recommend something simple like `password`.

* We are wanting to get to the following screen. Note your list on the left might vary depending on much you have previously used pgAdmin!

  * Note that pgAdmin loads in your default browser!

![pgAdmin First Screen](assets/JX-SP0-M0-01.png)

* Create a new server to connect to your app on Heroku
  * Right Click on `Servers`
  * From the context menu, choose `Create >` -> `Server...`

* Under the `General` Tab fill in `Name`. It can be any thing you want. Leave the rest as the defaults

![pgAdmin Server General](assets/JX-SP0-M0-02.png)

* Under the `Connection` tab
  * `Host name/address` is the host listed from Heroku, in my case `ec2-18-235-97-230.compute-1.amazonaws.com`
  * Leave the `Port` at `5432`
  * `Maintenance database` should be the database name from Heroku, in my case `d2puqdoih80btl`
  * `Username` is the username from Heroku, in my case `szpdsfwndvfcsb`
  * `Password` is the password from Heroku, in my case `759f951ea4289cabc53bb07128aa60675d2e17ee5e0f92a9d3e0020f831cff73`
    * Do check to `Save password?`

![pgAdmin Server Connection](assets/JX-SP0-M0-03.png)

* And finally under the `Advanced` tab
  * `DB restriction` should be set to the database name from Heroku. This makes finding your database on the server MUCH easier! In my case `d2puqdoih80btl`
* Now you can click `Save`!

![pgAdmin Server Advanced](assets/JX-SP0-M0-04.png)

* You should now be able to use this Heroku hosted PostgreSQL database like any local database!

</details>

</details>

---

<details>
<summary>Environment Variables</summary>

Environment variables have two parts, a name and value separated by an `=`. We use the value in our applications. We find out the value by reading the name. By convention, we make the variable name uppercase. The value is whatever case we need it to be.

* VariableName=VariableValue
* MYDBHOST=localhost

We will need some environment variables set up for the rest of the course. We will specifically need the following environment variables:

For using PostgreSQL with Spring

| Variable Name | Variable Value |
|---------------|----------------|
| MYDBHOST      | localhost      |
| MYDBNAME      | foundations    |
| MYDBUSER      | postgres       |
| MYDBPASSWORD  | password       |
MYDBPASSWORD is what ever you set up your PostgreSQL password to be!

For user authentication

| Variable Name     | Variable Value |
|-------------------|----------------|
| OAUTHCLIENTID     | lambda-client  |
| OAUTHCLIENTSECRET | lambda-secret  |

<details>
<summary>Environment Variables for Mac</summary>

![Video Lecture](assets/novideo.png)

To show what environment variables you currently have, from a terminal prompt enter

```BASH
printenv
```

To show the value of a specific environment variable, from a terminal prompt enter (where `path` is the variable name we are interested in). Case matters!

```BASH
echo $PATH
```

If nothing gets displayed, that environment variable is not set.

To set up permanently the environment variable will need in class, do the following:

* First you have decided if you need a `.bash_profile` or `.zprofile` configuration file
  * macOS Catalina and later uses the .`zprofile`
  * macOS Mojave and earlier uses the `.bash_profile`
  * It is not wrong to have both. I will be setting up both with the following instructions. You can just do the one for your macOS

* Make sure you have the right configuration file in your home directory.

```BASH
cd
touch .bash_profile
touch .zprofile
```

* Open the `.bash_profile` file for editing

```BASH
open .bash_profile
```

* This opens the `.bash_profile` file in your default text editor. Go to the bottom of the file and add the following lines.
  * Note: The value (text to the right of the = ) for `MYDBPASSWORD` will be whatever password you set when you installed PostgreSQL
  * The rest should be entered as is
  * We will make use of these environment variables later in the course!

```TEXT
export MYDBHOST=localhost
export MYDBNAME=foundations
export MYDBUSER=postgres
export MYDBPASSWORD=password
export OAUTHCLIENTID=lambda-client
export OAUTHCLIENTSECRET=lambda-secret
```

* Save the `.bash_profile` file

* Open the `.zprofile` file for editing

```BASH
open .zprofile
```

* This opens the `.zprofile` file in your default text editor. Go to the bottom of the file and add the following lines.
  * Note: The value (text to the right of the = ) for `MYDBPASSWORD` will be whatever password you set when you installed PostgreSQL
  * The rest should be entered as is

```TEXT
export MYDBHOST=localhost
export MYDBNAME=foundations
export MYDBUSER=postgres
export MYDBPASSWORD=password
export OAUTHCLIENTID=lambda-client
export OAUTHCLIENTSECRET=lambda-secret
```

* Now save the file and RESTART YOUR COMPUTER.
* After restarting you computer, use the commands from above to check on the values of the environment variables!

</details>

<details>
<summary>Environment Variables for Windows</summary>

![Video Lecture](assets/novideo.png)

To show what environment variables you currently have, from a command prompt enter

```BASH
set
```

To show a the value of a specific environment variable, from a command prompt enter

```BASH
set path
```

If nothing gets displayed, that environment variable is not set.

To set up permanently the environment variable will need in class, do the following:

* Note: When entering the environment variables below, the value (text to the right of the = ) for `MYDBPASSWORD` will be whatever password you set when you installed PostgreSQL
  * The rest should be entered as is
  * We will make use of these environment variables later in the course!

* Goto Control Panel -> System -> Advanced System Settings -> Environment Variables
  * In the System variable group at the bottom of the page
    * Click New...
      * For the variable name enter `MYBDHOST`
      * For the variable value enter `localhost`
      * Click Ok
    * Repeat those steps for each of the following environment variables - clicking New... and entering the information! Case MATTERS!
      * Variable Name is `MYDBNAME` | Variable value is `foundations`
      * Variable Name is `MYDBUSER` | Variable value is `postgres`
      * Variable Name is `MYDBPASSWORD` | Variable value is `password`
      * Variable Name is `OAUTHCLIENTID` | Variable value is `lambda-client`
      * Variable Name is `OAUTHCLIENTSECRET` | Variable value is `lambda-secret`

  * Click OK from the next screen
* And Click OK one more time

* Now RESTART YOUR COMPUTER.
* After restarting you computer, use the commands from above to check on the values of the environment variables!

</details>

<details>
<summary>Environment Variables for Ubuntu</summary>

![Video Lecture](assets/novideo.png)

To show what environment variables you currently have, from a terminal prompt enter

```BASH
printenv
```

To show a the value of a specific environment variable, from a terminal prompt enter

```BASH
echo $PATH
```

If nothing gets displayed, that environment variable is not set.

To set up permanently the environment variable will need in class, do the following:

* Make sure you have the `.bashrc` file in your home directory.

```BASH
cd
touch .bashrc
```

* Open the `.bashrc` file for editing. Nano is my favorite Linux editor! of course you can use the editor of your choice!

```BASH
nano .bashrc
```

* This opens the `.bashrc` file. Go to the bottom of the file and add the following lines.
  * Note: The value (text to the right of the = ) for `MYDBPASSWORD` will be whatever password you set when you installed PostgreSQL
  * The rest should be entered as is
  * We will make use of these environment variables later in the course!

```TEXT
export MYDBHOST=localhost
export MYDBNAME=foundations
export MYDBUSER=postgres
export MYDBPASSWORD=password
export OAUTHCLIENTID=lambda-client
export OAUTHCLIENTSECRET=lambda-secret
```

* Now save the file (using, if editing with Nano)
  * Type `Ctrl-x`
  * Type `y` to save
  * Press `Enter`

* Now RESTART YOUR COMPUTER.
* After restarting you computer, use the commands from above to check on the values of the environment variables!

</details>

</details>
