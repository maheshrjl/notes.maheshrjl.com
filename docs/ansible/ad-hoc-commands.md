# ℹ Playbook Options

**Syntax: ansible-playbook -i \[inventory] \[Options]**

### Playbook Options <a href="#playbookoptions" id="playbookoptions"></a>

|         Options        | Description                                                                                                    |   |
| :--------------------: | -------------------------------------------------------------------------------------------------------------- | - |
|     --syntax-check     | perform a syntax check on the playbook, but do not execute it                                                  |   |
|        --version       | show program’s version number, config file location, module search path, module location & executable location |   |
|       -C, --check      | don’t make any changes; instead, try to predict some of the changes that may occur                             |   |
|       -D, --diff       | when changing (small) files and templates, show the differences in those files; works great with –check        |   |
|      -b, --become      | run operations with become (does not imply password prompting)                                                 |   |
|  -K, --ask-become-pass | ask for privilege escalation password                                                                          |   |
|     -T , --timeout     | override the connection timeout in seconds (default=10)                                                        |   |
|    -e, --extra-vars    | set additional variables as key=value or YAML/JSON, if filename prepend with @                                 |   |
|      -f , --forks      | specify number of parallel processes to use (default=5)                                                        |   |
|      --flush-cache     | Clear the fact cache for every host in inventory                                                               |   |
|    --force-handlers    | Run handlers even if task fails                                                                                |   |
|      --list-hosts      | List matching hosts                                                                                            |   |
|      --list-tasks      | List all tasks that would be executed                                                                          |   |
|      --private-key     | Use this file to authenticate the connection                                                                   |   |
|         --step         | One step at a time, confirm each task before running                                                           |   |
|      -v, --verbose     | verbose mode (-vvv for more, -vvvv to enable connection debugging)                                             |   |
|    --ask-vault-pass    | Ask for vault password                                                                                         |   |
|      --become-user     | Run operations as this user (default=root)                                                                     |   |
|     --become-method    | privilege escalation method to use (default=sudo), use _ansible-doc -t become -l_ to list valid choices.       |   |
| --become-password-file | Pass a password file for the playbook                                                                          |   |
|       --vault-id       | the vault identity to use                                                                                      |   |
|    --vault-pass-file   | vault password file                                                                                            |   |