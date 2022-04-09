## Lab Report 1: Remote Access
***
![Image](https://wallpapercave.com/uwp/uwp1772743.gif)

*Downloading VS Code*
1. Go to [VS CODE](https://code.visualstudio.com/)  
2. Press the blue download button at the top left 
3. Follow the insturctions given by the site
4. Open on your PC and it should look like this 
(VS screen shot)

*Remotely Connecting*
1. Open VS Code Terminal (Command + ' or Terminal then New Terminal)
2. Then in your termial type ssh and then "cs15lsp22zz@ieng6.ucsd.edu", except replace zz with the 3 letters for your login
3. It will then ask for you to input your password
4. If this is your first connecting, you might get a message saying:
> "The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
> RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
> Are you sure you want to continue connecting (yes/no/[fingerprint])?"
if this is the case then press yes. 
5. Once you are connected to the remote server it should look like this:
> ![Image](SSH-Connect.png)

**YOURE NOW CONNECTED!!!**

![Image](https://c.tenor.com/ywS9vxQ2sqgAAAAM/smile-dancing.gif)

*Trying some commands*
Try these commads in your remote access termial!
- cd (name of folder) - change directory
- ls - list of files or direcorties 
- ls -lat - directory size 
- ls -a - gives all files inclding hidden ones(those with dots in the beginning)
>what it should it look like
>![Image](Commands.png)

*Moving files using scp*
- the command scp can ne inputed in your terminal to copy and paste a file and it will always run from your personal computer
1. Create a java file on your computer (or use one that has all already been made) and have the following code written in it:

         
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
2. After this in the terminal not connected to remote access write *scp <filename>.java cs15lsp22zz@ieng6.ucsd.edu:~/*
>remember to chnage zz to the correct letters for your login
3. you should be prompted with a password that you will enter again which will log you into ieng6.
4. type ls into the terminal after logging in
5. <filename>.java should be visible in your directory!
6. now run it using javac followed by java
> it should look like this!
![Image](scp.png)

**YOU HAVE SUCCESFULLY COPIED AND PASTED A FILE TO IENG6!!**
         
![Image](https://c.tenor.com/ZkMfy0jHXM0AAAAM/peach-goma.gif)
         
*Setting an SSH Key*
         

        
