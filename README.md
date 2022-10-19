ansible requires python 3.8 to be available at 

```/usr/bin/python```

and python 3.10 will give you the error
```ImportError: cannot import name 'Mapping' from 'collections'```

example
```
ansible -i hosts all -u root -k -m ping
SSH password:
 [WARNING]: sftp transfer mechanism failed on [127.0.0.1]. Use ANSIBLE_DEBUG=1 to see detailed information [WARNING]: scp transfer mechanism failed on [127.0.0.1]. Use ANSIBLE_DEBUG=1 to see detailed information127.0.0.1 | FAILED! => {
    "changed": false,
    "module_stderr": "Shared connection to 127.0.0.1 closed.\r\n",
    "module_stdout": "Traceback (most recent call last):\r\n  
    File \"/tmp/ansible_6nuwg4n8/ansible_module_ping.py\", 
    line 62, in <module>\r\n    from ansible.module_utils.basic import AnsibleModule\r\n  
    File \"/tmp/ansible_6nuwg4n8/ansible_modlib.zip/ansible/module_utils/basic.py\", 
    line 80, in <module>\r\n
    ImportError: cannot import name 'Mapping' from 'collections' (/usr/lib/python3.10/collections/{}init{}.py)\r\n",
    "msg": "MODULE FAILURE",
    "rc": 1
}
```
