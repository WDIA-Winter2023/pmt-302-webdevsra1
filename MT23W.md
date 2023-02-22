## CST 8254 Practical Mid Term

**Your Name:**

```

```

Answer directly in this .md file.

### Task 1:

1. Install Raspberry Pi OS using Raspberry Pi Imager  [https://www.raspberrypi.org/software/ 
   Select Raspberry Pi OS and recommended software from the first dropdown list.
2. If you have a keyboard, a mouse, a TV with hdmi input and access to your router, plug all the cables and proceed to step 4 with the installation.
3. If you want to do a keyboardless, screenless, wireless install:

   - Use the settings button to setup the pi name (**it must be your two initials followed by your student number**). wireless settings and password.

   - If you have a windows machine, **install OpenSSH**, start Settings then go to Apps > Apps and Features > Manage Optional Features. Scan this list to see if **OpenSSH client** is already **installed**. If not, then at the top of the page select "Add a feature", then: To **install** the **OpenSSH client**, locate "**OpenSSH Client**", then click "**Install**".

   - Get the IP address of your Pi by issuing the command `ping username.local` from a Terminal window/Command prompt window.
   
   - Then issue the command `ssh pi@<ipAddressOfYourPi>` where<ipAddressOfYourPi> is the Ip obtained from the previous step.
5. Start a terminal session then type `sudo raspi-config` . Navigate the various menu options to 

   - make sure that SSH, VNC, SPI, I2C are enabled. 
   - make sure you boot automatically in the GUI using the user pi.
   - set the time zone.

### Task 2:

On your pi, issue the following commands one by one in sequence

```
hostname -I
df
pwd
date
```

Take a screenshot  **start.jpg**,  and upload the jpg file to GitHub **NOW**.

On your laptop, in the folder of your choice, create a text file whose name is the concatenation of your firstname and your lastname . For example mine would read **`jeromemizon.txt`**. Open the file and add a line saying that you were there. For instance mine would read: **`Jerome Mizon was there.`**

Make sure your Pi is connected on your home network.

Using ``scp`` , send a copy of the file to your raspberry pi. **What command did you use?**

**1. **

```

```

Open a **`putty/ssh`** session to your raspberry pi .

**2. What command do you use to see a directory listing that includes the permissions of the files?**

```

```

Redo the last command and save the output of the command to a file **`pr1.txt`**. **What command did you use?**

**3. **

```

```

**4. What are the permissions of the file you just created?**

```

```

**5. What command do you use to display the folder you are currently working from?**

```

```

Change the permissions of the file so that group members can only execute it. **What command did you use?** 

**6. **

```

```

Create a folder **`midtermExam`** under the current working directory of your raspberry pi. **What command did you use?**

**7. **

```

```

**8. What are the permissions of this folder `midtermExam` ?**

```

```

**9. What command do you use to list the ports your raspberry pi is listening to? Try it using the `-at` flag.**

```

```

Redo the last command saving the output of the command to a file **`pr2.txt `**. **What command did you use?**

**10.**

```

```

On your laptop create a text file **`midtermPi.txt`**. The content of the file is a line stating that you were there. For instance mine would read: `**Jerome Mizon was there.**` Save the file.

From the command line start a sFTP session to your raspberry PI . **What command did you use to connect?**

**11. **

```

```

Copy the file **`midtermPi.txt`** to your PI using sFtp. **What command did you use?** 

**12. **

```

```

On your PI  run the following command

```
pwd>mt.txt;tree -l>>pr.txt
```

**13. **What does the command do?

```

```

Using `useradd`, create a user named after you using the concatenation of your firstname and last name. **What command did you use?**

**14. **

```

```

Create the home directory for the user you just created and change the ownership of this folder to the user himself/herself. **What commands did you use?**

 **15. **

```

```

Update your PI package list using `apt-get` , then use `apt-get` to install `Filezilla` on your  PI. **What commands did you use?**

**16. **

```

```

**17. ** issue the following command on your pi:

`cd /home`

`ls -als > /home/pi/pr3.txt`

### Task 3:

Install the following packages on your Pi using `apt-get`. Install them in the following order

1. Start by issuing the following commands from a terminal/command prompt window.
   `sudo apt-get update`
   `sudo apt-get upgrade`

2. Apache2: `sudo apt-get install apache2 -y`

3. Mariadb: `sudo apt-get install mariadb-server`

   Once installed, issue the following commands one by one from a terminal/command prompt window. Make sure you replace 'password' with a password of your choice.

   ```
   sudo mysql
   
   CREATE USER 'pi'@'localhost' IDENTIFIED BY 'password';
   
   GRANT ALL PRIVILEGES ON * . * TO 'pi'@'localhost';
   
   FLUSH privileges;
   
   EXIT;
   sudo service mysql restart
   ```

4. Php: `sudo apt-get install php`

5. Phpmyadmin: `sudo apt-get install phpmyadmin`
   Install it on the pi Apache web server.

From your laptop, connect to the pi phpmyadmin site using the ip address of your pi. Make a screenshot and name the screenshot `phpmyadmin.jpg`. Note that the screenshot must show the address bar of your browser.

### Task 4:

Intall a copy of Wordpress on your Pi.

The following site will assist you:

https://projects.raspberrypi.org/en/projects/lamp-web-server-with-wordpress/5

When setting up the wordpress database, log on using the user you created instead of using the`root` user as specified.

Install wordpress.

From your laptop, connect to the pi wordpress site using the ip address of your pi. Log on the wordpress site. Make a screenshot and name the screenshot `wpress.jpg`.  Note that the screenshot must show the address bar of your browser.

### Final Steps:

On your PI run the following commands

```
cd ~
ls -l > pr4.txt
cat /etc/passwd | tail -n2 > pr5.txt
```

On your pi, issue the following commands one by one in sequence

```
hostname -I
df
pwd
date
```

Take a screenshot  **end.jpg**,  and upload the jpg file to GitHub **NOW**.

------

Using `sftp` or `Filezilla`, transfer the files **`pr.txt,pr1.txt,pr2.txt,pr3.txt,pr4.txt,pr5.txt` to your laptop then upload them to GitHub. No Zip file, only text files, ******zip files will not be graded**.** 

**Upload the two jpg files wpress.jpg and phpmyadmin.jpg to GitHub.**

----------

**Edit this md file to only include the questions numbers and your answers as in .**

**1.**

```

```

**2. What command do you use to see a directory listing that includes the permissions of the files?**

```

```



Rename the file to `yourname.md` where yourname is the concatenation of your first name and last name. Then upload the file to GitHub.