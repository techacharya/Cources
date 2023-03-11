# Accessing the linux Command-line Terminal

Once we have done with the linux based operating system installation the next step is to access the linux command-line terminal. The power of linux system actually lies in it's command-line mode. Graphical User Interface is very simple to learn and use. There are three different method by which command-line can be accessed:
  - Text mode
  - GUI mode
  - Remote access over Secure Shell 

If you're at the physical console or in the case of a **_Virtual Machine_**, the virtual console, you'll either get a login prompt if the system set defaults to the **` multi-user.target `** or a nice GNOME login window if it set defaults to the **` graphical.target `**.

### Using text mode
For many reasons, linux system may be configured to boot to a text login. If linux system is installed with the **_Minimal Install_** environment, it won't have a graphical mode at all. You can also set the system to default to **` multi-user `**, even if a **_GUI_** is there.

Getting to a command prompt is easy. Just enter your username don't forget it's case-sensitive; **_acharya_** and **_Acharya_** are not the same. Press **` Enter `**, and then type your password. Don't panic if you don't see any stars or other input as you type; **_linux_** doesn't display any password placeholder characters.

![command-line terminal](../../images/command-line/text-command-prompt.png)


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


Here, **[acharya@techacharya ~]$** represents the below details: <br>
**_acharya_**     ---> is the logged in user name <br>
**_techacharya_** ---> is a hostname <br>
**_~_**           ---> represents the logged in user's home directory or the present working directory and <br>
**_$_**           ---> denotes that logged in user is **_non-root_** user inplace of **$** if it is **#** then represents **_root_** user.

![command-line terminal](../../images/command-line/command-prompt-info.png)

### Super user and non-root user
Super user or administrator and not-root user can be differenciate by looking the either user name or by command prompt

![command-line terminal](../../images/command-line/root-nonroot.png)

### Remote access over Secure Shell 
In real world **_linux sysadmin_** often access the command prompt remotely only. Linux in text-mode configuration offers an almost identical experience when accessing the system remotely. Assume you are accessing your linux system from another system that could be either **_linux machine_** or **_Windows machine_** or from **_Mac OS_**. All you need to know is **_username_**, **_password_**, and the remote system's _**IP address or hostname_**. just follow the following:
  - From **_Windows system:_** open the **` Command Prompt (CMD) `** and type: <br>
    **_Syntax:_**
    ```
    > ssh username@linux_system-IP or hostname
    ```
    **_Example:_**
    ```
    > ssh acharya@192.168.70.130
    ```
    Accept the fingerprint by typing **_yes_** and hit **_Enter_** then provide ther **_acharya_** user's password. And you will land to linux command prompt. <br>

    If **_ssh_** command is not installed in **Windows** then you can use the **_putty Utility_** to access linux system. <br>
    Just download the **_Putty Utility_** and run the putty and fill the **_username_**, **_hostname or IP adsress_** of remote linux system and click on **` Open `** and then **` Accept `** the fingerprint.
    ![command-line terminal](../../images/command-line/access-from-putty.png)

    Now it's time to provide user's password, post entering the password press **_Enter_** key and you will land to command prompt.

    ![command-line terminal](../../images/command-line/terminal-putty.png)
  - From another **_Linux system_** just launch the command prompt and type the following:
    ```
    $ ssh acharya@192.168.70.130
    ```
    ![command-line terminal](../../images/command-line/remote-access.png)
  - From **_Mac OS_** just launch terminal and follow the same step as access from **_linux system_**.


### Exit or Logout from Terminal
There are a few ways to disconnect from it properly:
  - You can type either **` exit `** or **` logout `** and press **_Enter_**. 
  - Or you can press **` Ctrl + D `** on your keyboard.

### Virtual Terminal
A virtual or pseudo terminal allows a machine to connect to a remote server, usually to allow different user login or to run different application on single machine at a time. You can switch between these terminals using key combination **` Ctrl + Alt + f1 `** to **` Ctrl + Alt + f6 `**.

![command-line terminal](../../images/command-line/pseudo-terminal.png)

### Terminal Multiplexer (tmux)
**` tmux `** is a **_Terminal Multiplexer_** which, allows to create several **_pseudo terminals_** from a single terminal. This is very useful for running multiple programs with a single connection, such as when you're remotely connecting to a machine using **_Secure Shell (SSH)_**.

You can detach **` tmux `** from the current terminal, and all your programs will continue to run safely in the background. Later, you can reattach tmux to the same or a different terminal.

Some of **_tmux's_** features are as follows:
  - Fully customizable status bar
  - Multiple window management
  - Splitting window in several panes
  - Automatic layouts
  - Panel synchronization
  - Scriptability, which allows to create custom **_tmux_** sessions for different purposes

![command-line terminal](../../images/command-line/tmux-eg.png)

To start using **` tmux `**, type tmux on your terminal. This command launches a tmux server, creates a default session **_number 0_** with a single window, and attaches to it.
```
$ tmux
```
You can detach from your tmux session by pressing **_Ctrl + B_** then **_d_**. <br>
The **_tmux_** operates using a series of keybindings (keyboard shortcuts) triggered by pressing the **` prefix `** combination. By default, the prefix is **_Ctrl + B_**. After that, press **_d _** to detach from the current session.
```
[detached (from session 0)]
```
It's no longer attached to the session, but your long-running command executes safely in the background. You can list active tmux sessions with **_tmux ls_**:
```
$ tmux ls
```
**_0: 1 windows (created Sat Mar 11 15:15:33 2023)_** <br>

You can disconnect your **_SSH connection_** at this point, and the command will continue to run. When, reconnect to the server and reattach to the existing tmux session to resume where you left off:
```
$ tmux attach -t 0
```
#### tmux keybindings
The tmux provides several keybindings to execute commands quickly in a tmux session. Here are some of the most useful ones.

First, create a new **_tmux session_** if you're not already in one. You can name your session by passing the parameter **` -s name `**  to the **` tmux new `** command when creating a new session:
```
$ tmux new -s docker
```
| **Prefix** | **Combination** | **Description**                                            |
|------------|-----------------|------------------------------------------------------------|
| Ctrl + B   | D               | Detach from the current session.                           |
| Ctrl + B   | %               | Split the window into two panes horizontally.              |
| Ctrl + B   | "               | Split the window into two panes vertically.                |
| Ctrl + B   | Arrow Key (Left, Right, Up, Down) | Move between panes.                      |
| Ctrl + B   | X               | Close pane.                                                |
| Ctrl + B   | C               | Create a new window.                                       |
| Ctrl + B   | N or P          | Move to the next or previous window.                       |
| Ctrl + B   | 0 (1,2...)      | Move to a specific window by number.                       |
| Ctrl + B   | :               | Enter the command line to type commands. Tab completion is available. |
| Ctrl + B   | ?               | View all keybindings. Press Q to exit.                                |
| Ctrl + B   | W               | Open a panel to navigate across windows in multiple sessions.         |


#### Configure tmux
The **_tmux_** configuration can be changed permanently by modifying the **` tmux configuration `** file. By default, this file is located at **_$HOME/.tmux.conf_**.

**_For example:_** <br>
The default prefix key combination is **_Ctrl + B_**, but it can be changed to some other combination to convinient.

#### Customize the status bar
The **_tmux's_** status bar is fully customizable. You can change the colors of each section and what is displayed. 

Status bar can be changed by updating the status bar colors. First, enter command mode by typing **_Ctrl + B_** then **_:_** then change the colors with these commands:
  - To change the status bar background color: **` set -g status-bg cyan `**
  - Change inactive window color: **` set -g window-status-style bg=yellow `**
  - To change active window color: **` set -g window-status-current-style bg=red,fg=white `**




