ZeroStack Post Install Test
===========================

A set of small tests to ensure your ZeroStack cluster is running properly.

**Dependencies**

In order to run the post install tests download the cloud admin RC and certificate files out of the admin.local BU.

1. Zerostack rc file
2. Zerostack certificate file

**RC and Cert Files**

Pull the RC file from the newly installed ZeroStack cluster.

LogIn -> Click on BU List -> Click on admin.local BU -> Click on Project -> zs_default -> More tab -> API

When you get the RC file, make sure to specify your password and the fully qualified path to the cert file.

Set the OS_REGION variable to the name of your region.

**Run Tests**

$ source ~/zsrc.txt

$ zs-post-install

If you have already run the test, and would like to run it again, delete the PostInstall BU tat was created.

**OS Requierments**

CentOS 7

$ yum install -y epel-release,python-pip,hdparm

Ubuntu 14.04 / 16.04 / 18.04

$ apt install -y python-pip

**Pre-flight Prerequisites**

PIP will install all of the packages needed to run the ZS-Post-Install test, if they are not present.

$ pip install urllib3==1.24.1

**Installing**

To install the preflight check on the system, follow these steps. Make sure all of the pre-requisite packages have been installed.


$ pip install zs-postinstall-test


**Running the tests**

Run the post install test with the following command.


$ zs-post-install

Build and Submit
----------------

**GIT - development / nightly**

1. git clone https://github.com/Zerostack-open/post-install-test.git
2. cd zs-post-install-test
3. python setup.py bdist_wheel

**PIP - Development**

1. sudo python -m pip install --upgrade pip setuptools wheel
2. sudo python -m pip install tqdm
3. sudo python -m pip install --user --upgrade twine


Authors
-------


**Jonathan Arrance** - *Initial work* - [Zerostack-open](https://github.com/Zerostack-open)


See also the list of [contributors](https://github.com/JonathanArrance) who participated in this project.


License
-------

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/Zerostack-open/zs-post-install-test/blob/master/LICENSE) file for details
