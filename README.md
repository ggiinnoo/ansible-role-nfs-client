NFS client
=========

This playbook allows you to install and configure NFS shared

TODO
----

No to do's

Requirements
------------

There are no requirements for this role


Role Variables
--------------

This is an example of a full script install

    nfsShares:
      - name: "/nfs-share" # name on the nfs server
        server: "10.14.14.5" # nfs server ip or hostname
        path: "/nfs-mount" # where to mount
        version: "4" # nfs version
        opts: "defaults,rsize=65536,wsize=65536"
        state: "mounted" # Default mounted

The last 3 vars are default's and are not required to be fileld in.

Dependencies
------------

There are no Dependecies for this role

Example Playbook
----------------

    - name: Configure scripts
      hosts: all
      roles:
        - ggiinnoo.nfs_client

License
-------

BSD

Author Information
------------------

    Creator: Gino Jansen
    Website: www.ginojansen.nl
