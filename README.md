Sets up something similar to ansible-pull but not quite.

* Playbooks, roles, etc. gets pushed TO the host
* Only the hostvars for that host is pushed TO the host
* Sets up a couple of systemd-timers to run the playbooks on an interval

This means we can ensure the state of the host without exposing secrets
that are outside of the hosts own hostvars.
