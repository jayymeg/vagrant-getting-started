**LAB GUIDE**

**Installation**

Install and configure Vagrant on your Operating system.

**Documentation**

Add a step-by-step documentation of your output to your project submission file

1. Install Vagrant
    - Link: [**_Vagrant Downloads_**](https://developer.hashicorp.com/vagrant/downloads)
        - The link above redirects to the Vagrant official page for downloads.
    - Below is the output you’ll get from downloading from the CLI.
2. Verify the Installation
    - After installing Vagrant, verify the installation worked by opening a new command prompt or console, and checking that Vagrant is available.
        - Tip: If you receive an error that Vagrant is not found, try logging out and logging back into your system (particularly necessary for Windows).
    - $ vagrant
3. Create a directory
    - Make a new directory for the project you will work on throughout these tutorials.
    - $ mkdir vagrant_getting_started
    - Move into your new directory.
    - $ cd vagrant_getting_started
4. Initialize the project
    - Vagrant has a built-in command for initializing a project, vagrant init, which can take a box name and URL as arguments. Initialize the directory and specify the hashicorp/bionic64 box.
    - $ vagrant init

A Vagrantfile has been placed in this directory. You are now ready to vagrant up your first virtual environment! Please read the comments in the Vagrantfile as well as documentation on vagrantup.com for more information on using Vagrant.

1. Use a Box
    - Now you've added a box to Vagrant either by initializing or adding it explicitly, you need to configure your project to use it as a base. Open the Vagrantfile in any text editor and replace the contents with the following.
    - Vagrant.configure("2") do |config|
    - config.vm.box = "hashicorp/bionic64"
    - end

The hashicorp/bionic64 in this case must match the name you used to add the box above. This is how Vagrant knows what box to use. If the box was not added before, Vagrant will automatically download and add the box when it is run.

1. Bring up a virtual machine
    - Run the following from your terminal:
    - $ vagrant up

This command downloads the specified base box (if not already downloaded) and creates a virtual machine instance based on your configuration. In less than a minute, this command will finish and you will have a virtual machine running Ubuntu. You should have an Ubuntu box installed on your vagrant if all works well.

- - Once the virtual machine is running, SSH into the virtual machine:
    - $ vagrant ssh

This command opens a shell session within the virtual machine.

- - Explore the virtual machine environment, run commands, and perform any necessary configurations.

1. Stop and Destroy the Vagrant Virtual Machine:
    - To stop the virtual machine, run:
    - $ vagrant halt

This command gracefully shuts down the virtual machine.

- - To completely destroy the virtual machine, freeing up resources, run:
    - $ vagrant destroy

Confirm the action when prompted.


![vagrant lab guide 1](https://github.com/jayymeg/vagrant_getting_started/blob/master/images/vagrant%20lab%20guide%201.png)
![configuration of vagrantfile](https://github.com/jayymeg/vagrant_getting_started/blob/master/images/configuration%20of%20vagrantfile.png)
![vagrant lab guide 2]
