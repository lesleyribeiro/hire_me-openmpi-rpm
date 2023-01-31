# hire_me-openmpi-rpm

Hi James, sorry for my delay... the biggest problem was my weed-work. A lot of things to do!
But, I would like to you know, that I do my best, although short time...

# INSTRUCTIONS TO INSTALL
1. Use the following command to clone git:
$ git clone https://github.com/lesleyribeiro/hire-me_openmpi-rpm-repo.git

2. Go to "hire_me-openmpi-rpm" directory:
$ cd hire_me-openmpi-rpm

3. Execute the following command to install:
$ rpm -ivh openmpi-4.1.4-1.el7.x86_64.rpm


# HOW OPENMPI RPM WAS DID

The OpenMPI package was built using the following steps:

Install the RPM building tools on the Centos system by running the command:
$ yum install rpm-build
Create the necessary directories for building the RPM package using:
$ mkdir -p ~/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}

Downloaded the source code for OpenMPI version 4.1.4 from the OpenMPI website and placed it in the "~/rpmbuild/SOURCES" directory
$ wget https://download.open-mpi.org/release/open-mpi/v4.1/openmpi-4.1.4.tar.gz -P ~/rpmbuild/SOURCES

Created a spec file for the package in the "~/rpmbuild/SPECS" directory.
Built the RPM package by running the command:
rpmbuild -bb ~/rpmbuild/SPECS/openmpi.spec

The built package was found in the "~/rpmbuild/RPMS" directory with the name "openmpi-4.1.4-1.el7.x86_64.rpm"

Uploaded the RPM package to this Github repository.


# Little comment...
at least... for me it works fine :D

$ cd hire_me-openmpi-rpm/
$ ls
openmpi-4.1.4-1.el7.x86_64.rpm  README.md

$ rpm -ivh openmpi-4.1.4-1.el7.x86_64.rpm
Preparing...                          ################################# [100%]
Updating / installing...
   1:openmpi-4.1.4-1.el7              ################################# [100%]
$ rpm -qa | grep openmpi
openmpi-4.1.4-1.el7.x86_64

