fl.sshkey
=========

This role replace the user's ~/.ssh/authorized_keys file, or just add a new public ssh key to it

Requirements
------------

ssh keys file (standard openssh format)  

Role Variables
--------------

sshkey_clean : True or False : Remove the user's authorized_keys file, default=False  
ssh_user : the user to operate, default=root  

Files
------------
Files of keys should be present in the role files directory,  
and named : authorized_keys.<user name>  

example : authorized_keys.root for the user root  


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: fl.sshkey }

command line exemple:  
ansible-role fl.sshkey --hosts ubuntu --extra-vars "ssh_user=ansible"  

License
-------

GPLv3

Author Information
------------------

Fabrice LEGRAND : Computer Engineer  
see blog (in french) at https://fabsystem.wordpress.com/
