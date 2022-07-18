# 🐬 Ansible Snippets

{% code title="Disable pipelining when requiretty enablederett" %}
```yaml
- lineinfile:
    dest: /etc/sudoers
    line: 'Defaults requiretty'
    state: absent
  sudo_user: root
  vars:yam
      ansible_ssh_pipelining: no
```
{% endcode %}
