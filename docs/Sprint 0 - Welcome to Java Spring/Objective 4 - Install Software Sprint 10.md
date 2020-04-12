# Install Software Needed for this Sprint

* Java Development Kit (JDK)
* A Text Editor - Instructor will use Sublime - Your pick and you are on your own for installation!
* JetBrains IntelliJ IDEA Ultimate Version
* Postman - An API Client

Note that some of the Training Kit materials uses animated GIFs to highlight certain aspects of the curriculum. Many plugins, extensions, exits to control the playback of animated GIFs. The one I am using is GIF Scrubber. Look for it in your favorite plugin, extension, store!

<details>
<summary>JDK</summary>

Any version of JDK 8 or later should work with our code. Most people have the Java Runtime Environment Installed. We need the next level, the actual JDK.

The general download site for the JDK is [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)

<details>
<summary>JDK for Mac</summary>

![Video Lecture](assets/novideo.png)

* From the Website [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)
  * Pick the first link that says **Oracle JDK: JDK Download**
  * On the next page, click on the file for **macOS Installer**
  * Agree to the license agree and download the file.
  * Double click on dmg file that was just downloaded
  * We are going to install using the defaults suggested
  * Double click on the pkg file that appears
    * Click continue
    * Click install
      * You may have enter your password to install
    * Once installation is done, click close
      * I then choose to Move to Trash the installer

Let's try out our new installation. From a command prompt enter
    `java -version`
you will see something like `java version "14" 2020-03-17`. This should be the version of Java that you just installed and should closely match the next command's version.

From a command prompt enter
    `javac -version`
you will see something like `javac 14`. This should be the version of JDK that you just installed and should closely match the previous command's version.

If the above does not give you the correct version, but does give you a version, you have more that one Java Virtual Machine (JVM) installed on your computer.

* To get a list of the JVMs installed on your computer enter the command `/usr/libexec/java_home -V`
* You will need to make your new Java your main Java.
  * From a terminal prompt,
    * type `cd` to go to your root directory
    * Make sure you have a .bash_profile by entering the command `touch .bash_profile`
    * type `open .bash_profile` to edit your bash profile
    * In the file that opens, go to the bottom of the file and enter

```BASH
export JAVA_HOME=export JAVA_HOME='/usr/libexec/java_home -v 14'
```

Note: that 14 is the version of Java we just installed above.

* Save the file, restart your computer, and you should be good to go!
* For more information on this process, see [https://medium.com/@devkosal/switching-java-jdk-versions-on-macos-80bc868e686a](https://medium.com/@devkosal/switching-java-jdk-versions-on-macos-80bc868e686a)

For more information on installing the JDK, see [https://docs.oracle.com/en/java/javase/14/install/installation-jdk-macos.html](https://docs.oracle.com/en/java/javase/14/install/installation-jdk-macos.html)

</details>

<details>
<summary>JDK for Windows 10</summary>

![Video Lecture](assets/novideo.png)

* From the Website [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)
  * Pick the first link that says **Oracle JDK: JDK Download**
  * On the next page, click on the file for **Windows x64 Installer**
  * Agree to the license agree and download the file.
  * You will need to run the file
    * This can either be done as an option prior to downloading
    * Or you can launch the file after downloading

  * Install the software noticing the path where you install the software
  
  * Add the path to the TOP of the system PATH
    * Goto Control Panel -> System -> Advanced System Settings -> Environment Variables
      * In the System variable group at the bottom of the page, select the Path variable
        * Click Edit...
        * Click New
        * Enter the correct path for the bin folder of your JDK. It will look something like:
            `C:\Program Files\Java\jdk-14\bin`
          substituting your version number for the 14
        * Click outside the entry box
        * Using the Move Up button, move this directory to the TOP of your Path!
        * Click OK
      * Now let's add the JAVA_HOME environment variable
        * In System Variables, click New...
          * For the variable name enter `JAVA_HOME`
          * For the variable value enter `C:\Program Files\Java\jdk-14` - same directory at before without the `\bin`
          * Click Ok
      * Click OK from the next screen
    * And Click OK one more time
    * RESTART YOUR COMPUTER!!! Necessary for the Path change to take effect.

Let's try out our new installation. From a command prompt enter
    `java -version`
you will see something like `java version "14" 2020-03-17`. This should be the version of Java that you just installed and should closely match the next command's version.

From a command prompt enter
    `javac -version`
you will see something like `javac 14`. This should be the version of JDK that you just installed and should closely match the previous command's version.

If you do not get the correct version, retrace your installation steps paying particular attention to the Path variable's directory location!

For more information see [https://docs.oracle.com/en/java/javase/14/install/installation-jdk-microsoft-windows-platforms.html](https://docs.oracle.com/en/java/javase/14/install/installation-jdk-microsoft-windows-platforms.html)
</details>

<details>
<summary>JDK for Ubuntu</summary>

![Video Lecture](assets/novideo.png)

I do most of Linux from a terminal prompt!

Goto a terminal prompt and enter the following commands

```BASH
sudo add-apt-repository ppa:linuxuprising/java
sudo apt update
sudo apt install oracle-java14-installer
```

* You will need to agree to the Oracle License Agreement

Back to the terminal prompt, enter the following command

```BASH
sudo apt install oracle-java14-set-default
```

Let's try out our new installation. From a terminal prompt enter
    `java -version`
you will see something like `java version "14" 2020-03-17`. This should be the version of Java that you just installed and should closely match the next command's version.

From a command prompt enter
    `javac -version`
you will see something like `javac 14`. This should be the version of JDK that you just installed and should closely match the previous command's version.

If you do not get the correct version, retrace your installation steps!

</details>

</details>

---

<details>
<summary>IntelliJ</summary>

Home Page for JetBrains IntelliJ Idea [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/)

<details>
<summary>Installation of IntelliJ for all OS</summary>

IntelliJ Ultimate Edition is installed from your GitHub Student Pack

## To access the general benefits of GitHub Student Developer Pack

* Visit your Dashboard and click on the GitHub Student Developer Pack’s unique link. Once you click on it, do not do anything else in it.
* Visit [https://github.com/settings/billing](https://github.com/settings/billing).
  * At the bottom of this page, you should see that you have a coupon applied and when that coupon will expire.
    (Example of how the coupon should look: COUPON $7.00 off for 2 years until July 18, 2021.)
    If there is no coupon on there, you can use a new link that we can generate for you again. Be sure to reply back that you need it though.
  * Once you click on the new link, check the billing page again. If it says that it has been applied, then move onto the next step.
* Visit [education.github.com/pack/offers](education.github.com/pack/offers).
  You should be able to see that you can get your benefits there.
  (This is only the case if the coupon has been applied to your account, which is why you need to check the billing page first. Do not try to reapply or else that will mess up the system!)
* If, for some reason, you cannot access the benefits and are using Chrome, then please try using Firefox, Opera, or Safari instead. Highly recommend using Firefox for this though - even though you will normally see your instructor using Chrome in class!

## To access the JetBrains IntelliJ Ultimate benefit

* After doing the above!

* Please click on the card with the JetBrains logo.
* Authenticate with your GitHub credentials.
* You will be guided to a page on the JetBrains website where you can request your free educational license for JetBrains tools.
* You will get a series of two messages from the JetBrains team asking you to confirm your request and then to activate your educational JetBrains license.
* If, for some reason, this isn’t working, then please open up a support ticket with JetBrains.

</details>

<details>
<summary>Configuration of IntelliJ for all OS</summary>

Note: IntelliJ is highly configurable and you are encouraged to explore the configurations. For this section I showing you how to configure IntelliJ but not everything you may want to configure.

* Get to the IntelliJ Welcome Screen
* Click on the `Configure` option
* Select `Preferences`
  * Some items to consider
    * `General` -> `Code Folding`
      * I usually turn this all off except the option to Show code folding outline.
      * I am not a fan of hiding code.
    * `Font`
      * specifically allows you to change the font size
    * `Code Style` -> `Java`
      * Allows you to change how the code is reformatted when you do a Code Reformat.
    * `Plugins`
      * These are installed from the JetBrains Marketplace and allow you to greatly extend the capabilities of IntelliJ
      * We do not need any special Plugins for class but feel free to install and try some out!

* I have created an export of my Settings if you wish to use those. You can download these from [here](https://drive.google.com/open?id=1Z1Nek3sptA0PFJbCOP4-t_H5Qp-Kj4xa)
* To import these settings, from the Welcome Screen
  * Select `Configure` -> `Import Settings`
  * Pick the file you want to import, in this case `intellij_settings_from_john.zip`
  * From the check list, pick which settings you wish to import
  * Click OK and enjoy your new settings!
  * Yes, you will have to restart IntelliJ for these settings to take affect.

For more information see [https://www.jetbrains.com/help/idea/configuring-project-and-ide-settings.html](https://www.jetbrains.com/help/idea/configuring-project-and-ide-settings.html)
</details>

</details>

---

<details>
<summary>Postman</summary>

Website for Postman is [https://www.postman.com](https://www.postman.com)

<details>
<summary>Postman for Mac</summary>

![Video Lecture](assets/novideo.png)

* Surf to the website [https://www.postman.com](https://www.postman.com)
* Click on the **Download the App** button
  * It should default to the Mac version. If not click on the link for the Mac version
  * Double click on file that was just downloaded
  * Agree to open even though it was downloaded from the scary internet!
  * On the next screen, click the button Move to Applications Folder
  * You will be prompted to create a Postman account
    * You are welcome to do this, I just signed on using a Google Account
    * If you do not wish to create an account, goto to the pull down menu `Postman` -> `Quit Postman`
  * If needed, launch Postman from its icon ![Postman](assets/postman.png)
    * If an update is available, it will get quickly installed and you are ready to work with Postman!

</details>

<details>
<summary>Postman for Windows 10</summary>

![Video Lecture](assets/novideo.png)

* Surf to the website [https://www.postman.com](https://www.postman.com)
* Click on the **Download the App** button
  * It should default to the Windows version. If not click on the link for the Windows version
  * Click on Download -> Windows 64 bit
  * You will need to run the file
    * This can either be done as an option prior to downloading
    * Or you can launch the file after downloading
    * This does a nice installation
  * You will be prompted to create a Postman account
    * You are welcome to do this, I just signed on using a Google Account
    * If you do not wish to create an account, goto to the pull down menu `File` -> `Exit`
  * If needed, launch Postman from its icon ![Postman](assets/postman.png)
    * If an update is available, it will get quickly installed and you are ready to work with Postman!

</details>

<details>
<summary>Postman for Ubuntu</summary>

![Video Lecture](assets/novideo.png)

I will use snap to install Postman so from the terminal prompt enter the command

```BASH
snap install postman
```

* You will need to launch Postman from its icon ![Postman](assets/postman.png)
  * You will be prompted to create a Postman account
    * You are welcome to do this, I just signed on using a Google Account
    * If you do not wish to create an account, goto to the Application menu `Postman` - `Quit`
* You can relaunch Postman and be good to go!

</details>

</details>
