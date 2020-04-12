# Install Software Needed for this Sprint

* Heroku Access Including Heroku CLI

<details>
<summary>Heroku Cloud Account</summary>

![Video Lecture](assets/novideo.png)

You will need to create an Heroku Account. This is a free account and does not even require a credit card to get started!

* Surf to [https://www.heroku.com](https://www.heroku.com)
* Click on the `Sign up` button
* On the next screen, fill in the appropriate information
  * For company name you can enter Lambda School
  * For Role you can be a Student
  * Pick Java for Primary development language
* You will be sent an email to confirm your account
* Once you confirm you account - by clicking on the link from the email
  * You will be asked to set a password.
  * You will click on the button to Proceed and be taken to your Heroku dashboard!

Note: If Heroku ever asks you for a credit card number, you are at the wrong place! You do not need to give Heroku a credit card number for the work we do in class!

</details>

---

<details>
<summary>Heroku CLI</summary>

The installation of Heroku requires that Git be installed on your system. You probably already have it installed!

* On a Mac, you will need to install the Xcode Command Line Tools. You can do this by
  * in a terminal prompt, enter `git --version`
  * A dialog box will popup where you can click `Install` to install the Xcode Command Line Tools.
* Windows we normally install Git Bash from Git for Windows. See [https://gitforwindows.org/](https://gitforwindows.org/)
* For Ubuntu See [https://help.ubuntu.com/lts/serverguide/git.html](https://help.ubuntu.com/lts/serverguide/git.html)

<details>
<summary>Heroku for Mac</summary>

![Video Lecture](assets/novideo.png)

* Surf to the site [https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)
* Scroll down and find the button for macOS installer.
* Click that button and download the file.
* Double click on the pkg file that just downloaded
  * Yes it is safe to open, so click `Open`
  * Click Continue
  * Click Install
  * You might have to enter your password
  * Once Heroku CLI is installed, click Close
* Now go to a terminal prompt and type  

```BASH
heroku version
```

* You should get back something like  
    `heroku/7.35.1 darwin node-v12.13.0`  
  Your numbers may vary!

</details>

<details>
<summary>Heroku for Windows 10</summary>

![Video Lecture](assets/novideo.png)

* Surf to the site [https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)
* Scroll down and find the button for Windows 64-bit installer.
* Click that button
* You will need to run the file
  * This can either be done as an option prior to downloading
  * Or you can launch the file after downloading
* Take the defaults and when the installation is complete, click Close to end the installation
* Now go to a command prompt and type  

```BASH
heroku version
```

* You should get back something like  
    `heroku/7.39.1 win32-x64 node-v12.13.0`  
  Your numbers may vary!

</details>

<details>
<summary>Heroku for Ubuntu</summary>

![Video Lecture](assets/novideo.png)

* I am going to use snap to install the Heroku CLI on Ubuntu. So from a terminal prompt, enter

```BASH
sudo snap install --classic heroku
```

* Now from a terminal prompt and type

```BASH
heroku version
```

* You should get back something like  
    `heroku/7.39.1 linux-x64 node-v12.13.0`  
  Your numbers may vary!

</details>

</details>
