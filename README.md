# Puppet Infrastructure
This repository contains Puppet manifests for managing user accounts and setting up a LAMP stack.

## Purpose
The purpose of this repository is to provide a structured and automated approach to configuring and managing server environments using Puppet. It simplifies the process of setting up user accounts and installing a LAMP (Linux, Apache, MySQL, PHP) stack, ensuring consistency and efficiency in server management.

## What It Does
- User Management: Defines and ensures the presence of specific user accounts on the server.
- LAMP Stack Setup: Automates the installation and configuration of the necessary packages and settings for a fully       
  functional LAMP stack.
- Testing Environment: Includes a test PHP page to verify the successful installation and configuration of the LAMP stack.

# Contents
- server_users_groups.pp: Defines the user accounts that should be present on the server.
- lamp_stack_server.pp: Defines the packages and configurations required for setting up a LAMP stack.
- phpinfo.php: A test PHP page for verifying the PHP setup.

## To use these manifests, follow these steps:

- Clone the Repository:
  - git clone https://github.com/getac020/PuppetRepo.git
  - cd PuppetRepo
- Apply the Manifests:
  -  Ensure you have Puppet installed on your server.
  -  Apply the server_users_groups.pp manifest to set up user accounts:
  -  sudo puppet apply server_users_groups.pp
- Apply the lamp_stack_server.pp manifest to set up the LAMP stack:
  - sudo puppet apply lamp_stack_server.pp
- Verify the Setup:
  - Navigate to your web server’s IP address or domain name in a web browser and load the phpinfo.php page to confirm PHP is     configured correctly:
    - http://<your-server-ip>/phpinfo.php

## Steps Taken for Assignment
- Created a new Ubuntu 24.04 Server and installed Puppet.
- Used the VM created in part 1as a "template VM" to clone another VM. 
- Used Puppet to add users to the system.
- Used Puppet to implement a LAMP stack.
