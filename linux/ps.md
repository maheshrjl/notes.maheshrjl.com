---
description: 'ps styles: -unix style; BSD style without dash; --GNU style;'
---

# 🗜 Processes

### PS Options

**Syntax: ps -\[options]**

|  -a | All users                                                                                         |
| :-: | ------------------------------------------------------------------------------------------------- |
|  -u | list the user who started the process or when -u user is specified list the process for that user |
|  -x | Processes not executed by current terminal                                                        |
|  -e | List all processes regardless of the terminal; alt: -A                                            |
|  -H | Display parent child relationship                                                                 |
|  -j | Jobs format                                                                                       |
|  -f | Format                                                                                            |

#### Useful ps variations:

* **ps axjf:** Show process relationship
* **ps aux:** Show username, pid, cpu & memory, start date, & also the command that started the process.
* **pgrep \[process]:** Get PID without using ps | grep \[process]

### **Foreground process**

|    ctrl+c    | Kill a foreground process \[SIGINT] stands for sig-interrupt |
| :----------: | ------------------------------------------------------------ |
|    ctrl+z    | Sleep a foreground process \[SIGSTOP]/\[SIGCONT]             |
| fg \[job-id] | Bring a background process to foreground                     |

**Note: To check sleeping process use jobs command.**

### **Background process**

|       &      | Execute a process in background. Appended at the end of command or script |
| :----------: | ------------------------------------------------------------------------- |
| bg \[job-id] | Run a process in background                                               |
| fg \[job-id] | Bring a background process to foreground                                  |

**Note: To check sleeping process use jobs command.**

### **Killing a process**

**kill \[kill-signal] \[pid]**

Using a kill command sends a kill signal: List all kill signals: kill -l. SIGTERM is the default kill signal

|   kill  | SIGTERM \[Kill a process nicely, process can refuse this] |
| :-----: | --------------------------------------------------------- |
| kill -9 | SIGKILL \[Kill forcefully]                                |

Killing with process name: **pkill \[kill-signal] \[name]**
