# 🐬 Ansible Snippets

#### Disable pipelining when requiretty is enabled

```yaml
- lineinfile:
    dest: /etc/sudoers
    line: 'Defaults requiretty'
    state: absent
  sudo_user: root
  vars:yam
      ansible_ssh_pipelining: no
```

