## Streamline SSH Configuration 

1) open up your terminal
2) in your terminal type ```cd .ssh```
3) check if you have a config file by typing ```open config```
4) if there is an error saying the file does not exist, in your terminal type ``` touch config```. This will create a new config file
5) once your config file is created type ```open config``` again. This should open your config file in a text editor. 
6) In the editor copy and paste (feel free to rename the host - first liine that says "Host" - to whatever you would like).
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22(your last 3 letters)
    IdentityFile ~/.ssh/id_rsa
```
it should look like this:

![Image](configkey.png)

once this is created you can now type ``` ssh ieng6``` (or whatever you named the host) into the terminal and your remote account should open!

![Image](streamline.png)

to copy and paste using the new key just type ```scp filename ieng6:~/```

![Image](scp.png)
 
 **And the file should be there**
 