# Accessing the linux Command-line Terminal

Once we have done with the linux based operating system installation the next step is to access the linux command-line terminal. The power of linux system actually lies in it's command-line mode. Graphical User Interface is very simple to learn and use. There are two different method by which command-line can be accessed:
  - Text mode
  - GUI mode

If you're at the physical console or in the case of a **_Virtual Machine_**, the virtual console, you'll either get a login prompt if the system set defaults to the **` multi-user.target `** or a nice GNOME login window if it set defaults to the **` graphical.target `**.

### Using text mode
For many reasons, linux system may be configured to boot to a text login. If linux system is installed with the **_Minimal Install_** environment, it won't have a graphical mode at all. You can also set the system to default to **` multi-user `**, even if a **_GUI_** is there.

Getting to a command prompt is easy. Just enter your username don't forget it's case-sensitive; **_acharya_** and **_Acharya_** are not the same. Press **` Enter `**, and then type your password. Don't panic if you don't see any stars or other input as you type; **_linux_** doesn't display any password placeholder characters.


### Using GUI mode
If linux system is installed with **_Server with GUI_** base envirnment , it should include the **` X Window System `**, which is the **_GUI_**. The login looks as you might expect. Just select your username in the list to be prompted for your password. 

![GUI login prompt](../../images/command-line/gui-login.png)

Type the password you will see dots as you enter your password here, unlike at the text login and press the **` Sign In `** button or hit **` Enter `**.

![GUI login prompt](../../images/command-line/gui-login-passwd.png)

This process gets you to the desktop, but you're not at a command prompt yet. To access the command prompt click on the **` Activities `** menu in the upper-left.

![GUI login prompt](../../images/command-line/gui-activities.png)


Now click on the **_Terminal_** icon in the bottom menu in **_GNOME_** shell.

![GUI login prompt](../../images/command-line/run-terminal.png)

This step launches the **_GNOME Terminal_**, and now you're at a command prompt.

![GUI login prompt](../../images/command-line/terminal-prompt.png)


![command-line terminal](../../images/command-line/text-command-prompt.png)

Here, **[acharya@techacharya ~]$** represents the below details: <br>
**_acharya_**     ---> is the logged in user name <br>
**_techacharya_** ---> is a hostname <br>
**_~_**           ---> represents the logged in user's home directory or the present working directory and <br>
**_$_**           ---> denotes that logged in user is **_non-root_** user inplace of **$** if it is **#** then represents **_root_** user.

![command-line terminal](../../images/command-line/command-prompt-info.png)

