---
description: 'ps styles: -unix style; BSD style without dash; --GNU style;'
---

# 🗜 processes

### <mark style="color:blue;">PS Options</mark>

**Syntax: ps -\[options]**

|  -a | All users                                                                                         |
| :-: | ------------------------------------------------------------------------------------------------- |
|  -u | list the user who started the process or when -u user is specified list the process for that user |
|  -x | Processes not executed by current terminal                                                        |
|  -e | List all processes regardless of the terminal; alt: -A                                            |
|  -H | Display parent child relationship                                                                 |
|  -j | Jobs format                                                                                       |
|  -f | Format                                                                                            |

{% hint style="info" %}
See which program this port belongs to: `lsof -i tcp:80`
{% endhint %}

#### Useful ps variations:

* **ps axjf:** Show process relationship
* **ps aux:** Show username, pid, cpu & memory, start date, & also the command that started the process.
* **pgrep \[process]:** Get PID without using ps | grep \[process]

### <mark style="color:purple;">**Foreground process**</mark>

|    ctrl+c    | Kill a foreground process \[SIGINT] stands for sig-interrupt |
| :----------: | ------------------------------------------------------------ |
|    ctrl+z    | Sleep a foreground process \[SIGSTOP]/\[SIGCONT]             |
| fg \[job-id] | Bring a background process to foreground                     |

**Note: To check sleeping process use jobs command.**

### <mark style="color:orange;">**Background process**</mark>

|       &      | Execute a process in background. Appended at the end of command or script |
| :----------: | ------------------------------------------------------------------------- |
| bg \[job-id] | Run a process in background                                               |
| fg \[job-id] | Bring a background process to foreground                                  |

**Note: To check sleeping process use jobs command.**

### <mark style="color:red;">**Killing a process**</mark>

**kill \[kill-signal] \[pid]**

Using a kill command sends a kill signal: List all kill signals: kill -l. SIGTERM is the default kill signal

|        kill       | SIGTERM \[Kill a process nicely, process can refuse this] |
| :---------------: | --------------------------------------------------------- |
|      kill -9      | SIGKILL \[Kill forcefully]                                |
| fuser -k filename | Kill a process that is ocking a file                      |

Killing with process name: **pkill \[kill-signal] \[name]**

{% hint style="info" %}
Kill a process running in port: `kill -9 $(lsof -t -i:8080)`
{% endhint %}
