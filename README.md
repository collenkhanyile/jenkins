# jenkins
creating my first jenkis


You have been asked to install and configure a Jenkins server so that your team can use it in order to do continuous integration.

In order to accomplish this, you will need to:

Install Java JDK 8 or later
Configure the Jenkins YUM repository
Install Jenkins from the YUM repository
Enable and start the Jenkins service
Get the temporary admin password and use it to log in to Jenkins
Install the default plugins
Create a permanent administrator account
Some useful links:

Installing Jenkins on RedHat distributions: https://wiki.jenkins.io/display/JENKINS/Installing+Jenkins+on+Red+Hat+distributions
Jenkins installation documentation for other environments: https://jenkins.io/doc/book/installing/
UPDATE: use the package jenkins-2.277.4-1.1 when installing Jenkins.


Install Jenkins in the learning activity environment
Install Jenkins in the learning activity environment via the YUM package manager. You must first configure the Jenkins YUM repositories in order to do this. You can install Jenkins like so:

sudo yum -y install java-1.8.0-openjdk epel-release
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum -y install jenkins-2.277.4-1.1

Complete Jenkins setup in the browser
After installing and starting Jenkins, there is some setup that needs to be completed through the Jenkins web interface. You can access Jenkins at Jenkins Server Public IP:8080.

First, you will need to login using the temporary admin password, which you can find on the server with this command:

 sudo cat /var/lib/jenkins/secrets/initialAdminPassword
Then, select Install suggested plugins and wait for the plugins to finish installing.

Finally, you will need to fill out a form to create credentials for the first admin user.
