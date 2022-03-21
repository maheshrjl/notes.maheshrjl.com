---
cover: ../.gitbook/assets/A.jpg
coverY: 1.3816925734024181
---

# 🔏 Ad-Hoc Command Options

### Ad-Hoc Options

Syntax: **`ansible -i [inventory] [server group] -m [module] -u [user]`**

| Options | Description                                                                                                                   |
| :-----: | ----------------------------------------------------------------------------------------------------------------------------- |
|    -m   | Specify a module Eg:`-m command -a ping`                                                                                      |
|    -a   | Specify arguments for a module or use command module by default                                                               |
|    -f   | Specify number of `forks` ansible uses. 1 will send command to one server at a time in order hosts are arranged in inventory. |
|    -b   | Becomes a different user `root` by default. `--become` is used to supplement `sudo` when not operating with Linux systems.    |
|    -K   | Will ask the password for root user when used with `-b`. Alternative:`--ask-become-pass`                                      |
|    -u   | Specify a username Eg: `-u mhs`                                                                                               |
| --limit | Limits the host, command will not execute on the ip marked with limit. Also, supports regex for ip. Eg: `"ip1,ip2"`           |

#### Notes:

If module is not specified with -m **ansible defaults to the command module** for ad-hoc commands

**Command module doesn't support `|` & redirection**, use `-m shell` module

* Eg: `ansible all -m shell -a "command | grep text"`

### **Polling & running in Background:** <a href="#backgroundtasks" id="backgroundtasks"></a>

* **`-p 0`** Specify a polling time in seconds. Ansible will run the command in the background and check in the specified time if that command has executed.`0 = polling disabled`

Eg: **`ansible all -B 1800 -P 60 -a "/usr/bin/long_running_operation --do-stuff"`**

* This job runs for 30 minutes with polls every minute
* `-B` Specify time limit for the job to run in background.

Eg: **`ansible all -B 3600 -P 0 -a "/usr/bin/long_running_operation --do-stuff"`**

* This job runs for 3600 seconds without polling

> **Note:** A result file is printed in output which gives a job ID. Check the result of the job using **`ansible all -m async_status -a "jid=jobid"`**

* Job ID is unique to each server.
