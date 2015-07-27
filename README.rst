cli-github
============

**A Python App to display Github from the command-line!**

Click `here <https://github.com/harshasrinivas/cli-github/blob/master/images/my.gif>`__ to see it live in action!
-----------------------------------------------------------------------------------------

+-----------+--------------+
|  Version  |   Downloads  |
+===========+==============+
| |Version| |  |Downloads| |
+-----------+--------------+

Version 1.0.9
-------------
- Option to show the contents of a file/folder
- Conformed to pep8 guidelines
- URL input parsing made better
- List the user followers

Live Demo
=========

`DEMO <http://showterm.io/aaa79dee63aad0695e304#fast>`__ : Display the list of a user's repositories from the username/URL, along with the number of stargazers

`DEMO <http://showterm.io/99e16e6ae35727999eb23#fast>`__ : Display all the folders and files within a repository recursively from the repository URL, along with their sizes

`DEMO <http://showterm.io/820b37fab14c7ed4cf7ff#fast>`__ : To get the RAW version of the readme file of a repository from the repository URL

`DEMO <http://showterm.io/24a6ceec356bb672ec24f#fast>`__ : To get the list of releases from the user's repository URL

`DEMO <http://showterm.io/bb2245e764781b11b1b78#fast>`__ : Download the tarball from the user's repository URL

`DEMO <http://showterm.io/910e8e424f28cfe3b4a22#fast>`__ : Download the zipball from the user's repository URL

`DEMO <http://showterm.io/4dcfaca8c50f912e3c609#fast>`__ : To show the contents of a file/folder

`DEMO <http://showterm.io/9bfd25a48074fb2ca8211#fast>`__ : List the followers of the user

Installation
============

Using ``pip``
-------------

.. code:: sh

   $ pip install cli-github

Latest build from the Source
----------------------------

-  Clone the repo
   
   .. code:: sh
      
      $ git clone https://github.com/harshasrinivas/cli-github.git

-  Run 
   
   .. code:: sh
   
      $ python setup.py install

Dependencies
============

-  ``prettytable`` 
   
   .. code:: sh
   
      $ pip install prettytable


-  ``future``

   .. code:: sh
     
      $ pip install future

- ``python-dateutil``

  .. code:: sh

     $ pip install python-dateutil


Setting Up
==========

**Github Token as Permanent Environment Variable**

Set your Github Personal Access Token as the environment variable
GITHUB\_TOKEN

.. code:: sh

   $ echo "export GITHUB_TOKEN=<your-token-with-quotes>" | sudo tee -a /etc/environment

**Github Token as Temporary Environment Variable**

.. code:: sh

   $ GITHUB_TOKEN=<your-token-with-quotes>

**Without saving your Environment Variable**

.. code:: sh

   $ cat cli_github/mains.py | sed -e "s/API_TOKEN = os.environ.get('GITHUB_TOKEN')/API_TOKEN = <your-token-with-quotes>/" > cli_github/mains.py

Options
=======

.. code:: sh

    -h, --help            show this help message and exit
    -n URL, --url URL
                        Get repos from the user profile URL/username
    -r RECURSIVE, --recursive RECURSIVE
                        Get the file structure from the repo link URL
    -R README, --readme README
                        Get the raw version of the repository readme file from repo link URL
    -re RELEASES, --releases RELEASES
                        Get the list of releases from repo link
    -dt TARBALL, --tarball TARBALL
                        Download the tarball from repo link
    -dz ZIPBALL, --zipball ZIPBALL
                        Download the zipball from repo link
    -op OPENFILE, --openfile OPENFILE
                        Show the contents of the given file in a repo
    -f FOLLOWERS, --followers FOLLOWERS
                        Get followers of the user
    -j LANGUAGE, --jobs LANGUAGE
                        Get available jobs in programming language of your choice

Usage
=====

Display the list of a user's repositories from the username/URL

.. code:: sh

   $ cli-github -n harshasrinivas

Display all the files and folders within a repository recursively from
the repository URL

.. code:: sh

   $ cli-github -r harshasrinivas/cli-github

Get the RAW version of the readme file of a repository from the
repository URL

.. code:: sh

   $ cli-github -R harshasrinivas/cli-github

Get the list of releases from the user's repository URL

.. code:: sh

   $ cli-github -re harshasrinivas/cli-github

Download the tarball of the any repo

.. code:: sh

   $ cli-github -dt harshasrinivas/cli-github

Download the zipball of the any repo
 
.. code:: sh
   
   $ cli-github -dz harshasrinivas/cli-github

Show the contents of a file/folder
 
.. code:: sh
   
   $ cli-github -op harshasrinivas/cli-github/setup.py

List the followers of a user
 
.. code:: sh
   
   $ cli-github -f harshasrinivas

Get the list of available Jobs in your desired Programming language

.. code:: sh
   
   $ cli-github -j Python


Contribute
==========

If you want to add features, improve them, or report issues, feel free
to send a pull request.

Contributors
============

- `harshasrinivas <https://github.com/harshasrinivas>`__ 
- `sananth12 <https://github.com/sananth12>`__
- `SanketDG <https://github.com/SanketDG>`__
- `Pratik151 <https://github.com/Pratik151>`__
- `Tushar <https://github.com/tushar-rishav>`__

.. |Build Status| image:: https://travis-ci.org/harshasrinivas/cli-github.svg?branch=master
      :target: https://travis-ci.org/harshasrinivas/cli-github

.. |Version| image:: https://badge.fury.io/py/cli_github.svg
      :target: http://badge.fury.io/py/cli_github
      
.. |Downloads| image:: https://img.shields.io/pypi/dd/cli-github.svg
      :target: https://pypi.python.org/pypi/cli-github
