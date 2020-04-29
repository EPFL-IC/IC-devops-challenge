STI DevOps Challenge
===========

## The Challenge

Your challenge, should you choose to accept it, is to set up and
maintain sustainable infrastructure for a web application with _Ansible_ or _Docker_.
We like people who are able to learn and research. Even if you might
not get the tasks completed, write down the notes with desired
solution. Your notes will help us in the evaluation of your
work. We understand there's more than one way to do things. If you're
stuck, pick one and justify your choice.


## Specifications

Infrastructure should be created and managed by _Ansible_ or _Docker_. It should
contain at least 3 nodes:

- One balancer node with _Haproxy_ on board.
- One application node with a _Django_ application (should be served
  with nginx or Apache).
- One backend node with _Postgres_ or _MySQL_.

## Rules

### Ansible

- Ansible should build and run all infrastructure by one play.
- Ansible should install critical security patches for the OS.
- Ansible should update aplication code without any interruptions of
  service for end user.
- The Django application does not need to be complex or written
  specifically for this challenge. Feel free to take any ready-to-use
  opensourse application.
- Please try and complete the assessment within one week of receiving it.
- Explain your solutions in 2-3 lines.
- Create git repository to track and share your work. Please link
  commits relevant to each task completed. a private gitHub repository (there's no cost to
  you). Invite "jaepetto" to your repository team.
- Share your results even if you don't finish.

### Docker

- Use a `docker-compose` file to bring the whole infrastructure at once.
- You should provide a documentation on how to update the applications containers without an interruption of service.
- The Django application does not need to be complex or written
  specifically for this challenge. Feel free to take any ready-to-use
  opensourse application.
- Please try and complete the assessment within one week of receiving it.
- Explain your solutions in 2-3 lines.
- Create git repository to track and share your work. Please link
  commits relevant to each task completed. a private gitHub repository (there's no cost to
  you). Invite "jaepetto" to your repository team.
- Share your results even if you don't finish.


## How to use it

### Ansible

- Install _Virtualbox_ and _Vagrant_ on your machine.
- Ensure to have a RSA key stored under "~/.ssh/id_rsa.pub".
- Run this Vagrantfile using "vagrant up".

After running this Vagranfile you will have a Class-C private network
on the 192.168.50.0 subnet with the following FQDNs and IP address for each node:

- node-1.vagrant : 192.168.50.10
- node-2.vagrant : 192.168.50.11
- node-3.vagrant : 192.168.50.12

### Docker

you should probably know how to do that.


## Advices

- Feel free to add more features! Really, we're curious about what you
  can think of. We'd expect the same if you worked with us.
- Comment your solution, either with comments on your configs or in a
  separate documents' structure.
- Use all git tools to let us understand how you arrived to the
  solution. Preferrably, submit your solution with multiple consequent
  commits, and not just one.
- Be ready to answer any kind of questions about your solution.


## Bonus

- Increase failover by adding one or more application(s)/backend
  node(s) (create your own updated Vagrantfile to be able to build
  your infrastructure).
- Create _Ansible_ playbook for creating/restoring database backups.
