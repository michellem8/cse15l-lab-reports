# Lab Report 1: Remote Access
***
![Image](https://wallpapercave.com/uwp/uwp1772743.gif)

## Downloading VS Code
1. Go to [VS CODE](https://code.visualstudio.com/)  
2. Press the blue download button at the top left 
3. Follow the insturctions given by the site
4. Open on your PC and it should look like this 
![Image](VSCODE.png)

## Remotely Connecting
1. Open VS Code Terminal (Command + ' or Terminal then New Terminal)
2. Then in your termial type ```ssh``` and then ``cs15lsp22zz@ieng6.ucsd.edu``, except replace zz with the 3 letters for your login
3. It will then ask for you to input your password
4. If this is your first connecting, you might get a message saying:
```
"The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])?"
```
if this is the case type ```y```. 

5. Once you are connected to the remote server it should look like this:

![Image](SSH-Connect.png)

**YOURE NOW CONNECTED!!!**

![Image](https://c.tenor.com/ywS9vxQ2sqgAAAAM/smile-dancing.gif)

## Trying some commands

Try these commads in your remote access termial!
- ``cd`` - (name of folder) - change directory
- ``ls`` - list of files or direcorties 
- ``ls -lat`` - directory size 
- ``ls -a`` - gives all files inclding hidden ones(those with dots in the beginning)

**What it should it look like!**

![Image](Commands.png)

## Moving files using scp

The command ``scp`` can be inputed in your terminal to copy and paste a file and it will always run from your personal computer.

1. Create a java file on your computer (or use one that has already been made) and have the following code written in it:

         
```
class WhereAmI' {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
} 
```
2. after this in the terminal not connected to remote access write ```scp filename.java cs15lsp22zz@ieng6.ucsd.edu:~/```
         
         -remember to chnage zz to the correct letters for your login
3. you should be prompted with a password that you will enter again which will log you into ieng6
4. type ```ls``` into the terminal after logging in
5. filename.java should be visible in your directory!
6. now run it using ```javac``` followed by ```java```

**It should look like this!**

![Image](scp.png)

**YOU HAVE SUCCESFULLY COPIED AND PASTED A FILE TO IENG6!!**
         
![Image](https://c.tenor.com/ZkMfy0jHXM0AAAAM/peach-goma.gif)
         
## Setting an SSH Key
         
An ssh key allows you to copy and paste into the ieng6 server without having to enter a password. Here are the steps to do this:
        
1. on the client terminal (not logged into ieng6) enter: 
- ```ssh - keygen```
- ```/Users/user-name/.ssh/id_rsa```
- for this line ```'Enter passphrase (empty for no passphrase):``` ' and this ```"Enter same passphrase again:"``` just press enter twice
- you should get something that looks like this:
```
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local
The key's randomart image is:

         +---[RSA 3072]----+

         |                 |

         |       . . + .   |

         |      . . B o .  |

         |     . . B * +.. |

         |      o S = *.B. |

         |       = = O.*.*+|

         |        + * *.BE+|

         |           +.+.o |

         |             ..  |

         +----[SHA256]-----+
```

2. now you have to copy the public key to the ssh directory using:
- ```ssh cs15lsp22zz@ieng6.ucsd.edu```
- Enter your password
- ```mkdir .ssh```
- ```exit``` (brings you back to client)
then on the client 
- ```scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys```
3. once you follow these steps you should be able to use ```ssh``` or ```scp``` from client to server without entering your password. 
![Image](SSH-key.png)
         
         
         
## Optimizing Remote Running
         
Use what you have learned to make the proccess of copying and modifying files faster and easier!!

1. Once you follow the same steps as with the ssh key (above), you wont need to enter your password anymore which will make the switch from client to remote much more effiecnt. 
2. To optimize your remote running try entering a few things like: 
- ```scp filename.java cs15lsp22zz@ieng6.ucsd.edu```
 - ```ssh cs15lsp22zz@ieng6.ucsd.edu "ls"``` which will long into the remote server and list your directory
 - ```cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI``` semi-colons can run multiple commands on one line instead of having to enter each command on a new line
 - using the up arrow key will retrieve previous commands used in the terminal


         
![Image](Opt-run.png)

**And thats its youre done!!**

![Image](https://c.tenor.com/YdTpw-54DXcAAAAC/pusheen-laptop.gif)
         

         


         
  
         

        
