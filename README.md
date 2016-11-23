[![Build Status](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-flowdock.svg?branch=master)](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-flowdock)
ansible-role-flowdock
=========

Sends a flowdock notification. Nice to put at the end of an ansible-playbook to be informed when a play has completed.

Limitation
----------

If the role is put as the last, then if anything fails in the playbook - the flowdock notification will not be sent because the ansible-role-flowdock will not be executed.

Requirements
------------

ansible >=2.2

Role Variables
--------------

Token is found at https://www.flowdock.com/account/tokens

 - flowdock\_token: "TOKEN"
 - flowdock\_chat: True
 - flowdock\_from\_address: "change@example.com"

If chat is set to True it sends a flowdock chat message.
If False, we send an inbox message.

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-flowdock }


Output:
<pre>
Ansible Run Completed Successfully on my.example.com! 

ansible_root on 12:37 ansible

#my.example.com #example.com #ansible #siteName #ok

From:	ansible_root <change@example.com>

ansible successful on my.example.com as root. IPv4=10.1.1.1/255.255.255.0, IPv6=No IPv6/, biosdate=06/08/2015, biosversion=1.2.6, dist=CentOS, distversion=7.2.1511, kernel=3.10.0-327.18.2.el7.x86_64, memory=257854, processor=Intel(R) Xeon(R) CPU E5-2620 v3 @ 2.40GHz, git_head=devel, vendor=Dell Inc.
</pre>

License
-------

MIT

Author Information
------------------
