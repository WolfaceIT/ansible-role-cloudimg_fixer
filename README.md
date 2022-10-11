cloudimg-fixer
=========

Try to avoid fuckery when using cloud img / cloudinit, especially on Proxmox

Role Variables
--------------

`cif_no_deletekeys` adds `ssh_deletekeys=False` to cloud-init config to avoid deletion of SSH Host keys
`cif_create_swap` should we add swap?
```
# Options for the created swap, assumed in a file
cif_swap_options:
  type: file
  size: 1024
  path: path for file
cif_vim_editor: true
cif_qemu_agent: true
```
Example Playbook
----------------

Careful, though this role was imported in Galaxy/GitHub, this is hosted primarily on gitlab, so you'd need a requirements.yml like:
```
---
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

