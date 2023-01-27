# hire_me-openmpi-rpm

#The OpenMPI package was built using the following steps:

Hi James, sorry for my delay... the biggest problem was my weed-work. A lot of things to do!

But, I would like to you know, that I do my best, although short time...

Following steps that was did:
Install the RPM building tools on the Centos system by running the command "yum install rpm-build"
Create the necessary directories for building the RPM package using "mkdir -p ~/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}"

Downloaded the source code for OpenMPI version 4.1.4 from the OpenMPI website and placed it in the "~/rpmbuild/SOURCES" directory
Created a spec file for the package in the "~/rpmbuild/SPECS" directory.

Built the RPM package by running the command "rpmbuild -bb ~/rpmbuild/SPECS/openmpi.spec"

The built package was found in the "~/rpmbuild/RPMS" directory with the name "openmpi-4.1.4-1.el7.x86_64.rpm"
Uploaded the RPM package to this Github repository.
How to add the repository to your operating system:

Use the following command to clone git:
git clone https://github.com/lesleyribeiro/hire-me_openmpi-rpm-repo.git

and run this to install:
rpm -ivh openmpi-4.1.4-1.el7.x86_64.rpm


at least... for me it works fine :D

openmpi-4.1.4-1.el7.x86_64.rpm  README.md
[root@localhost hire_me-openmpi-rpm]# rpm -ivh openmpi-4.1.4-1.el7.x86_64.rpm 
Preparing...                          ################################# [100%]
Updating / installing...
   1:openmpi-4.1.4-1.el7              ################################# [100%]
[root@localhost hire_me-openmpi-rpm]# rpm -qa | grep openmpi
openmpi-4.1.4-1.el7.x86_64
[root@localhost hire_me-openmpi-rpm]# 
