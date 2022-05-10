# lab-report-3-week-6
## Streamlining ssh Configuration
First, I accessed .ssh/config file by VScode. 
I did this by opening the `.ssh` file with VScode, it is on my computer if I do `wenyingcao$ ls -la`, I will get `wenyingcao  staff    192 Apr 28 14:50 .ssh`.
![.ssh-file](the-.ssh-file-in-computer.png)
![.ssh-file](using-vscode-opening-.ssh-file.png)
Second, I used ssh command to log into the server with just the alias.
After I set the key in my `.ssh` file, I can log into my ucsd server using only `ssh ieng6` without typing in the rest of my user name. 
Third, scp command copying a file to your account. I used the command `scp <filename> ieng6:~` to copy file from my local computer to the ucsd server. I highlighted how I did it in the screeshot, and then in logged into the server using the alias to check if the file copied successfully.
![ucsd-server](logging-into-ieng6-with-just-the-alias-and-scp-file.png)
## Setup Github Access from ieng6
First, I set up the private key in ucsd server by using the command `ssh-keygen`
![setting-up](setting-private-key-to-github.png)
Then, I made use `ls` to see all the files to see where I stored the private key files. 
![private-key](private-key-location.png)
Then, I copied it to github
![github](public-key-locaiton-in-github.png)
To access GitHub form a server like `ieng6`, there are couple steps you need to follow.
First, we want to clone a GitHub repository into the `ieng6`. After we set up the `ssh` key to our GitHub settings, we can clone the GitHub repository into the `ieng6` with the ssh link without actually typing in password. One thing to keep in mind is to use the corrct link, there are `HTTPS`, `SSH` and `GitHub CLI` links, remember to copy the `SSH` link as the screenshot show.
![right-link](right-ssh-link-to-copy.png)
Thus, we want to use the command `git clone <SSH link>` as the following screenshot.
![clone-to-ieng6](git-clone-form-ing6.png)
Second thing we want to do is make a change, we cannot push or commit anything if there is no changes made. Thus we want to use this command `touch <file name>` to create a new file, in this case, we created a new file called file1 as the screenshot shown.
![create-file](create-new-file-form-ieng6.png)
The thrid thing we want to do is to add this file using the command `git add <file name>`
![git-add](git-add-form-ieng6.png)
The fourth thing we want to do is that to commit the changes, which is adding a new file, to the local repository. Remember there are two different command `commit` and `push`, the difference is that commit is committing to the local repository, and push is pushing to the GitHub repository. There is also something worth notice is that we want to do `git commit -m "massage we want to sent"` to commit.
![git-commit](git-commit-form-ieng6.png)
Then the last thing is to push to the GitHub repository. We want to use `git push` as shown.
![git-push](git-push-form-ieng6.png)