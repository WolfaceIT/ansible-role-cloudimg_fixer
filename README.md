cloudimg-fixer
=========

Try to avoid fuckery when using cloud img / cloudinit, especially on Proxmox

Role Variables
--------------

`cif_no_deletekeys` add `ssh_deletekeys=False` to cloud-init config
`cif_create_swap` should we add swap?
```cif_swap_options:
  type: file
  size: 1024
  path: path for file
  ```
Example Playbook
----------------

Careful, this is hosted primarily on gitlab, so you'd need a requirements.yml like:
```---
roles:
  - name: gilou.cloudimg_fixer
    src: https://gitlab.com/wolface/ansible-roles/cloudimg_fixer.git
```

```
    - hosts: servers
      become: true
      roles:
         - gilou.cloudimg_fixer
```

License
-------

WTFPL v2

Author Information
------------------

Gilou from Wolface.IT
