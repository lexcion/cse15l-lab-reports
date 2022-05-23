## Lab Report 3 - Justin He



## Streamlining my ssh Configuration

This is my .ssh/config file, which I edited through VSCode:

![Image](report3pictures/pic1.png)

To log into my ssh account with an alias, I used the command "ssh juh020@ieng6", juh020 being my alias, to log in like so: 

![Image](report3pictures/alias1.png)

Then I used this scp command to copy the file into my alias.

![Image](report3pictures/aliascopy.png)

Now when I log back into my alias and check the files, I can confirm that the testfile was successfully copied in:

![Image](report3pictures/aliasls.png)

## Setting up Github Access from ieng6

Using Github Bash, I can view the public keys stored on my user account (the files with .pub at the end):

![Image](report3pictures/pic4.png)

I also added the ssh key to my github:

![Image](report3pictures/publickey.png)

And this is the path where my private key is stored in my laptop: 

![Image](report3pictures/pic5.png)

To commit and push a change on github through my remote account, I first commited my MarkdownParse.java file which outputted this:

![Image](report3pictures/pic6.png)

Then I pushed the change using "git push origin main":
![Image](report3pictures/pic6.1.png)

The link of my commit that I did remotely can be found here:

[Commit link](https://github.com/lexcion/markdown-parser/commit/edd3534254ed18008655c6f9bbab6ab10f23d439)


## Copying whole directories with scp -r

I used a command to copy my markdown-parse directory to the remote account which outputted this:

![Image](report3pictures/pic7.png)

(And this):

![Image](report3pictures/pic8.png)

I was then able to log into my remote account, then compile and run the tests remotely:

![Image](report3pictures/pic9.png)

Lastly, after much trial and error I was able to copy the directory and then compile it in one long command like so: 

![Image](report3pictures/copyandrun.png)

Overall, in this lab I learned to more easily log in remotely, commit/push on github through the terminal, and copy/run a directory in the remote server.