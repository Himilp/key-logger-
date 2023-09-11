# A simple keylogger for Windows, Linux and Mac
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.png?v=103)](https://opensource.org/licenses/mit-license.php)


Welcome to the simple keylogger repo! A keylogger is a program that records your keystrokes, and this program saves them in a log file on your local computer.

Currently, there are three keylogger programs for the major operating systems; Windows, Mac and Linux.

## Windows
To change visibility of the window set the `#define` in line 9 to `visible` or `invisible`.

Simply compile into an .exe, and then run. Visual Studio is good for this.

- `invisible` makes the window of the logger disappear, and it also starts up hidden from view. Note that it is still visible in the task manager.
- `visible` is visible, and the window does not close when typing. Great for testing it out.

Both of these save the keystrokes to a .txt file when closed.

> Note that sometimes your compiler may through up errors. If it does, keep compiling - the program still works. As always, please create an issue if you have a problem.

## Mac
This is a little more complicated. Please note, it does not work for secure areas such as password inputs. I have not found a work around yet.

### Installation
Download the repo. It will install in `/usr/local/bin/keylogger`.

Install it:

`$ git clone https://github.com/GiacomoLaw/Keylogger && cd keylogger/mac`

`$ make && make install`

It will log to `/var/log/keystroke.log`. This may require root access, but you can change that if you want. Set where you want it to log:

`$ keylogger ~/logfile.txt`

`Logging to: /var/log/keystroke.log`

Want to make it start on system startup?

`$ sudo make startup`

That will run it on startup.

### Uninstall
`$ sudo make uninstall`

Will uninstall the program, but not the logs.

---

> Please note that this logger cannot record keystrokes in protected areas yet.

# Keylogger

**Keylogger** is simple keylogger for Windows, Linux and Mac.
## Installation

The following instructions will install Keylogger using pip3 .

```
  pip3 install -r requirements.txt
```
or 
```
  pip3 install pyxhook
```

## How to run it

By running `nohup python3 keylogger.py &` command, it'll start to log your strokes:
The meaning of nohup is ‘no hangup‘.
When nohup command use with ‘&’ then it doesn’t return to shell command prompt after running the command in the background. 
```
$~/Keylogger/linux$ nohup python3 keylogger.py &
[1] 12529 //this is the keylogger's PID (process ID)
$:~/Keylogger/linux$ fg

```

The Keylogger is now running! It will log your strokes to a file .
Stop it by typing the command `fg` then hitting `CTRL+C`

or

`kill {PID}` for example `kill 12529`


---

#### Uses

Some uses of a keylogger are:

- Business Administration: Monitor what employees are doing.
- School/Institutions: Track keystrokes and log banned words in a file.
- Personal Control and File Backup: Make sure no one is using your computer when you are away.
- Parental Control: Track what your children are doing.
- Self analysis

---

Feel free to contribute to fix any problems, or to submit an issue!

Please note, this repo is for educational purposes only. No contributors, major or minor, are to fault for any actions done by this program.

Help support the project:
