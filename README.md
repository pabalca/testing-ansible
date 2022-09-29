# testing-ansible

```
 $ ansible-playbook -i inventory/ site.yml -t radar -kK
/opt/homebrew/Cellar/ansible/5.7.1/libexec/lib/python3.10/site-packages/paramiko/transport.py:236: CryptographyDeprecationWarning: Blowfish has been deprecated
  "class": algorithms.Blowfish,
SSH password: 
BECOME password[defaults to SSH password]: 

PLAY [radar] ****************************************************************************************************

TASK [radar : create directory] *********************************************************************************
ok: [umbrel.local]

TASK [radar : clone repository] *********************************************************************************
ok: [umbrel.local]

TASK [radar : generate systemd unit] ****************************************************************************
ok: [umbrel.local] => (item=valencia)
ok: [umbrel.local] => (item=colonia)

TASK [radar : systemd reload] ***********************************************************************************
skipping: [umbrel.local]

TASK [radar : restart] ******************************************************************************************
skipping: [umbrel.local]

PLAY RECAP ******************************************************************************************************
umbrel.local               : ok=3    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0   
```
