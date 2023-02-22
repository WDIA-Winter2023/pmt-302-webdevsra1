## CST 8254 Practical Mid Term

**Your Name:**

```
Sravan Suresh
```

**1. **Using `scp` , send a copy of the file to your raspberry pi. **What command did you use?**

```
scp sravansuresh.txt pi@sravan1285.local:/home/pi
```

**2.**What command do you use to see a directory listing that includes the permissions of the files?

```
ls -l
```

Redo the last command and save the output of the command to a file **`pr1.txt`**. **What command did you use?**

**3.**

```
ls -l > pr1.txt
```

**4.**What are the permissions of the file you just created?

```
-rw-r--r--
```

**5.**What command do you use to display the folder you are currently working from?

```
pwd
```

Change the permissions of the file so that group members can only execute it. **What command did you use?**

**6. **

```
chmod g=x pr1.txt
```

Create a folder **`midtermExam`** under the current working directory of your raspberry pi. **What command did you use?**

**7. **

```
mkdir midtermExam
```

**8.**What are the permissions of this folder `midtermExam` ?

```
drwxr-xr-x
```

**9.**What command do you use to list the ports your raspberry pi is listening to? Try it using the `-at` flag.

```
netstat -at
```

Redo the last command saving the output of the command to a file **`pr2.txt `**. **What command did you use?**

**10.**

```
netstat -at > pr2.txt
```

On your laptop create a text file **`midtermPi.txt`**. The content of the file is a line stating that you were there. For instance mine would read: `**Jerome Mizon was there.**` Save the file.

From the command line start a sFTP session to your raspberry PI . **What command did you use to connect?**

**11. **

```
sftp pi@sravan1285.local
```

Copy the file **`midtermPi.txt`** to your PI using sFtp. **What command did you use?**

**12. **

```
put midtermPi.txt /home/pi/
```

**13. **What does the command do?

```
'pwd' command will print the working directory and save it to 'mt.txt'. And 'tree -l' will create a directory tree like structrue and save that to 'pr.txt'.
```

**14. **Using `useradd`, create a user named after you using the concatenation of your firstname and last name. **What command did you use?**

```
sudo useradd -m -s /bin/bash sravan_suresh
```

 **15. **Create the home directory for the user you just created and change the ownership of this folder to the user himself/herself. **What commands did you use?**

```
sudo mkdir /home/sravan_suresh
sudo chown sravan_suresh:sravan_suresh /home/sravan_suresh
```

Update your PI package list using `apt-get` , then use `apt-get` to install `Filezilla` on your PI. **What commands did you use?**

**16. **

```
sudo apt-get update
sudo apt-get install filezilla
```
