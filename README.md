PTP
=========

This role will install and configure PTP for Linux and Solaris 11 hosts. For RHEL it uses an RPM package provided on the role itself *** see files directory ***, for Solaris 11 it uses IPS package manager to download and install the PTP daemon.


Variables
--------------

defaults/main.yml contains the variables for both RHEL and Solaris 11 configuration values, and packages names.
vars/main.yml contains the custom-facts octet map

***  added a block statement on the tasks to identify if Solarflare driver is installed  ***

Dependencies
------------

- custom-facts

*** I've included the custom-facts role to run within this role. If that's not the preferred way then it needs to be removed from the tasks ***

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: custom-facts } *** see Dependencies note ***
         - { role: PTP }


Author Information
------------------

Ignacio Spinosa, UNIX Engineer, ITG Dublin.
