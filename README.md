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
