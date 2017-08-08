# Much Deploy

## Purpose

I'm currently iterating on a lot of ideas and needed to get a few
different kinds of servers in the wild. Each of these represents
some goal. I allowed my ansible to get rusty so I'm taking a look at some
old playbooks to get up to speed.

I don't expect it to be pretty but it sure damn better work.

## Ansible Philosophy

My ansible philosophy: Keep the size of roles to a minimum. Use them to install whatever
packages for that operating system and a baseline config, and that's it.

All granular configuration is done in tasks. Every application has a configuration
file that is copied over with the correct values.

This leads to a specific way of viewing a playbook. You see your roles
as all the `apt-get install commands` and basic configs or production baselines, if you will.
When you get to the tasks sections you see those as each configuration step away from the
base configuration of whatever you are changing.

This is also easily parsable and verifiable but that is a native benefit
from ansible and yml structure. I have no real argument for using this
structure over others other than we use a similar one at my company and it works. =)

## Playbook Table of Contents


### [Jupyterhub](jupyterhub.yml)

This is a pretty interesting playbook to explore some possibilities with
Jupyterhub. Jupyterhub allows you to start up single-session jupyter notebooks
for users. This seems like an excellent platform to place tutorials
and example code. GitHub renders jupyter notebooks and they are not only for
Python use. Julia and R are also supported kernels.


## A Special Thanks

I want to give a special thank you to the [PySlackers](https://pyslackers.com)
python slack community. I especially want to thank @mattrasband for his
awesome use of certbot. Thanks to @ovv for the reminder that tasks should be
indempotent ;).

