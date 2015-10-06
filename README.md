ansible-role-flowdock
=========

Sends a flowdock notification 

Requirements
------------

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

License
-------

MIT

Author Information
------------------
