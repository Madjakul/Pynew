# Pynew

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) ![GitHub contributors](https://img.shields.io/github/contributors/Madjakul/Pynew) ![code size](https://img.shields.io/github/languages/code-size/Madjakul/Pynew)

A bash script which creates a skeleton for your Python projects. Easy to use and ideal for students (assignments) and small projects.


## Prerequisites

Before you begin, ensure you have met the following requirements:

* Internet Connection
* A computer running under Linux or MacOS
* [Docker](https://phoenixnap.com/kb/how-to-install-docker-on-ubuntu-18-04)
* [pip](https://pip.pypa.io/en/stable/installing/)


## Installing pynew

* Create a ```bin``` folder in your home directory
```bash
mkdir ~/bin
```

* Add this directory to your path
```bash
nano ~/.bashrc
```
At the very end of the text edito, add this line
```bash
export PATH="$HOME/bin:$PATH"
```
Press <kbd>Ctrl</kbd> + <kbd>X</kbd> then <kbd>Y</kbd> and finally hit <kbd>Enter</kbd> in order to save the file.

* Load the new ```$PATH``` into the current shell session using the ```source``` command:
```bash
source ~/.bashrc
```
it will allow you to run the script from anywhere on your PC.

* You can now clone this directory wherever you want. From the local folder where you want it to be installed, copy the link under the "clone" button

* Once it's cloned, open your terminal from the installation folder and run
```bash
chmod u+x pynew.sh
```

* You can now run 
```bash
mv pynew.sh ~/bin
```
In order to move the pynew bash script to the bin directory you have just created.


## Using pynew

From the folder where you want your project's skeleton to be stored, simply run
```bash
pynew.sh
```


## Credits

This script creates a simplified skeleton, highly inspired from these articles :
* [Ultimate Setup for Your Next Python Project](https://towardsdatascience.com/ultimate-setup-for-your-next-python-project-179bda8a7c2c)
* [Automating Every Aspect of Your Python Project](https://towardsdatascience.com/automating-every-aspect-of-your-python-project-6517336af9da)


## Contact

If you want to contact me you can reach me at [@Madjakul](https://twitter.com/madjakul).

## License

This project uses the following license: [MIT](https://github.com/Madjakul/Pynew/blob/master/LICENSE)
