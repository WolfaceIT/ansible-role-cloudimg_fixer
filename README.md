cloudimg-fixer
=========

Try to avoid fuckery when using cloud img / cloudinit, especially on Proxmox

Role Variables
--------------

`cif_no_deletekeys` add `ssh_deletekeys=False` to cloud-init config
`cif_create_swap` should we add swap?
```cif_swap_options:
  type: partition|lv|file
  size: 1024
  vg: myvg #volumegroup?
  path: path for file
  ```
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - gilou.cloudimg_fixer

License
-------

WTFPL v2

Author Information
------------------

Gilou from Wolface.IT
