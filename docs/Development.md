# Development

## Introduction to orchestration

You may be a developer, or Linux sysadmin, but new to orchestration. As an
extremely quick primer, think of orchestration as a way to create one stonking
big configuration file, point it at a target and magically make that target into
whatever your configuration file describes.

This is orchestration in a nutshell. We have a set of definitions and our
orchestration framework applies those definitions to one or more targets, to
make them conform. This project uses configuration management, a type of
orchestration, to apply a configuration to one or more target computers.

One of the great beauties of orchestration is that it enables us to define our
infrastructure (networks, servers, workstations, whatever) *as code*. And
*that's* great because it means we can put the definitions into source control.
Different people can work on different parts of the configuration. We can roll
forwards and backwards through changes. We can have independent testing branches
and so on.

There are many orchestration systems available, all with different strengths and
specialties. You may have heard of Chef, Puppet, CFEngine, Terraform, Docker,
Vagrant or any of the other mainstream orchestration tools. 

## Getting started with Ansible

This project uses [Ansible](https://www.ansible.com/). Ansible is great for
controlling the configuration of servers and workstations. Compared to some of
the other orchestration systems, it's relatively easy to learn. It has a low
technical barrier to entry, too: all that's needed on the target machine is SSH
and Python, rather than a dedicated agent.

Ansible is used in complex, multicomponent cloud-based systems. But this is a
simple project, focused in most cases on configuring a single target computer.
So it's not necessary to learn all of Ansible's capabilities, to contribute to
this project.

Ansible is mature and well documented these days. The following resources should
help anyone wishing to dive in:

* [Official "Get started" documentation](https://www.ansible.com/resources/get-started)
* [Technical overview](https://www.ansible.com/overview/how-ansible-works)
* [Ansible modules index](https://docs.ansible.com/ansible/latest/modules/modules_by_category.html)

Additionally, see how this project is structured. There are a few files in the
root, but most of the 'work' sits under the ```roles``` directory. Different
aspects of the Special Needs Linux configuration are split up into separate
'roles'. So we have a role for installing and configuring the KDE desktop, a
role that sets up the main user of the system, a role that configures the
system's name, and so on. (Some of these roles may change or be refactored as
the project matures.)

## Contributing code to Special Needs Linux

Anyone is welcome to fork the entire project and set off on their own. That's
the beauty of open source - you can do what you like (except turn it into a
commercial package). If you come up with something special, we hope you'll
contribute that back to the original Special Needs Linux project, but there's no
obligation to do so.

To work on this project, get in touch with Rob (see the README), who will set
you up as a Github collaborator. All additions to the project should be
developed on a separate branch and submitted for approval as a pull request.

## Contributing anything else

Rob will be the first to admit he has virtually no graphics design skills and no
marketing ability. Whatsoever. All contributions are very welcome - desktop
backgrounds, a project icon, web design, etc. Drop a note to Rob (see the README
for contact details) and we'll work from there.

Thanks for your interest in Special Needs Linux!