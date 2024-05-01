ufw
===

Configure UFW firewall.

This role only opens TCP and UDP ports from public and a defined management network.

Notes
-----
If you want to reset and only open the ports from this role, run `ufw reset` beforehand. Ensure that you are still able to talk to the system before running this!

Role Variables
--------------

| Name                   | Comment                                           | Default value |
|------------------------|---------------------------------------------------|---------------|
| ufw_public_allowed_tcp | List of TCP ports to be allowed from anywhere     | `[]`          |
| ufw_public_allowed_udp | List of UDP ports to be allowed from anywhere     | `[]`          |
| ufw_mgmt_allowed_tcp   | List of TCP ports to be allowed from mgmt network | `[]`          |
| ufw_mgmt_allowed_udp   | List of UDP ports to be allowed from mgmt network | `[]`          |
| ufw_mgmt_my_iprange    | The mgmt IP range the target server lives in      | ``            |
| ufw_mgmt_src_iprange   | The mgmt IP range the connecting hosts live in    | ``            |
| ufw_forward_policy     | Should IP forwarding be enabled?                  | `false`       |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - oxivanisher.linux_server.ufw

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_server](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_server/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_server).
