# test-repo
test repo for pactice
How To Install and Configure GitLab on Ubuntu 16.04 -------

Installing the Dependencies

Before we can install GitLab itself, it is important to install some of the software that it leverages during installation and on an ongoing basis. Fortunately, all of the required software can be easily installed from Ubuntu's default package repositories.

Since this is our first time using apt during this session, we can refresh the local package index and then install the dependencies by typing:

    sudo apt-get update
    sudo apt-get install ca-certificates curl openssh-server postfix
    
Installing GitLab

Now that the dependencies are in place, we can install GitLab itself. This is a straight forward process that leverages an installation script to configure your system with the GitLab repositories.

Move into the /tmp directory and then download the installation script:

    cd /tmp
    curl -LO https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh
    
    Feel free to examine the downloaded script to ensure that you are comfortable with the actions that it will take. You can also find a hosted version of the script here:

    less /tmp/script.deb.sh

Once you are satisfied with the safety of the script, run the installer:

    sudo bash /tmp/script.deb.sh

The script will set up your server to use the GitLab maintained repositories. This lets you manage GitLab with the same package management tools you use for your other system packages. Once this is complete, you can install the actual GitLab application with apt:

    sudo apt-get install gitlab-ce

This will install the necessary components on your system.
