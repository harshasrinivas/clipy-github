#`cli-github`

**A Command-Line Python Application to display Github from the CLI !**



|  Version |  Downloads  |
| -------- |  ---------  |
| [![PyPI version](https://badge.fury.io/py/cli_github.svg)](http://badge.fury.io/py/cli_github) | [![PyPi downloads](https://img.shields.io/pypi/dd/cli-github.svg)](https://pypi.python.org/pypi/cli-github)

![gif](https://github.com/harshasrinivas/cli-github/blob/master/images/my.gif)

##Version 1.0.9
* List the contents of a given file/folder
* Conformed to pep8 guidelines
* URL input parsing made better
* List User followers

#Installation

##Using `pip`

`pip install cli-github`

##Get the latest build from the Source

* Clone the repo `git clone https://github.com/harshasrinivas/cli-github.git`
* Run `python setup.py install`

##Dependencies

* prettytable `pip install prettytable`
* future `pip install future`
* python-dateutil `pip install python-dateutil`

#Setting Up

**Github Token as Temporary Environment Variable**

`$ GITHUB_TOKEN=<your-token-with-quotes>`

**Github Token as Permanent Environment Variable**

`$ echo "export GITHUB_TOKEN=<your-token-with-quotes>" | sudo tee -a /etc/environment`

**Without saving your Environment Variable**

`$ cat cli_github/mains.py | sed -e "s/API_TOKEN = os.environ.get('GITHUB_TOKEN')/API_TOKEN = <your-token-with-quotes>/" > cli_github/mains.py`

<br>

#Options

```sh
-h, --help          show this help message and exit
-n URL, --url URL   
					Get repos from the user profile URL/USERNAME
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
```



#Usage

Display the list of a user's repositories from the username/URL, along with the number of stargazers

`$ cli-github -n harshasrinivas`

Display all the files and folders within a repository recursively from the repository URL, along with their sizes

`$ cli-github -r harshasrinivas/cli-github`

Get the RAW version of the readme file of a repository from the repository URL

`$ cli-github -R harshasrinivas/cli-github`

Get the list of releases from the user's repo link

`$ cli-github -re harshasrinivas/cli-github`

Download the tarball of the any repo

`$ cli-github -dt harshasrinivas/cli-github`

Download the zipball of the any repo

`$ cli-github -dz harshasrinivas/cli-github`

List the contents of the given folder

`$ cli-github -op harshasrinivas/cli-github/setup.py`

Get the list of followers of the user

`$ cli-github -f harshasrinivas`

Get the list of available Jobs in your desired Programming language

`$ cli-github -j Python`

#Live Demo

[**DEMO**](http://showterm.io/aaa79dee63aad0695e304#fast) : Display the list of a user's repositories from the username/URL, along with the number of stargazers

[**DEMO**](http://showterm.io/99e16e6ae35727999eb23#fast) : Display all the folders and files within a repository recursively from the repository URL, along with their sizes

[**DEMO**](http://showterm.io/820b37fab14c7ed4cf7ff#fast) : To get the RAW version of the readme file of a repository from the repository URL

[**DEMO**](http://showterm.io/24a6ceec356bb672ec24f#fast) : To get the list of releases from the user's repository URL

[**DEMO**](http://showterm.io/bb2245e764781b11b1b78#fast) : Download the tarball from the user's repository URL

[**DEMO**](http://showterm.io/910e8e424f28cfe3b4a22#fast) : Download the zipball from the user's repository URL

[**DEMO**](http://showterm.io/4dcfaca8c50f912e3c609#fast) : Show the contents of a given file/folder

[**DEMO**](http://showterm.io/9bfd25a48074fb2ca8211#fast) : List the followers of a user

#Contribute

If you want to add features, improve them, or report issues, feel free to send a pull request.

#Contributors

* [harshasrinivas](https://github.com/harshasrinivas)
* [sananth12](https://github.com/sananth12)
* [SanketDG](https://github.com/SanketDG)
* [Pratik151](https://github.com/Pratik151)
* [Tushar](https://github.com/tushar-rishav)

#License

![GPL V3](https://raw.githubusercontent.com/harshasrinivas/cli-github/master/images/gpl.png)
