# Pynew
![GitHub](https://img.shields.io/github/license/Madjakul/Pynew) ![GitHub contributors](https://img.shields.io/github/contributors/Madjakul/Pynew) ![code size](https://img.shields.io/github/languages/code-size/Madjakul/Pynew)

A bash script which creates a skeleton for your Python projects. Easy to use and ideal for students (assignments) and small projects.

## Prerequisites

Before you begin, ensure you have met the following requirements:

* Internet Connection
* A computer running under Linux or MacOS

## Installing pynew

If you want to use latest version, install from source. To install pynew from source, follow these steps:

* From the local folder where you want it to be installed, copy the link under the "clone" button
* Open your terminal and run 
```bash
find "$(cd ..; pwd)" -name "filename"
```
You will see the absolute Path that leads to the pynew.sh script.
* Copy the path to your clipboard and run
```bash
PATH=$PATH:/path/to/pynew.sh
```
it will allow you to run the script from anywhere on your PC.
* Finally, you need to change the permissions of the script otherwise it wont work. From the folder where the script is intalled, run
```bash
sudo chmod 774 pynew.sh
```

## Using pynew

From the folder where you want your project's skeleton to be stored, simply run
```bash
bash pynew.sh
```

For some syntaxe matters, I could'nt fill the Makefile with some default features. Copy this to your Makefile
```mk
MODULE := ###

BLUE='\033[0;34m'
NC='\033[0m' # No Color

install-requirements:
    pip3 install -r requirements.txt

run:
    @python3 -m $(MODULE)

test:
    @pytest

lint:
    @echo "\n${BLUE}Running Pylint against source and test files...${NC}\n"
    @pylint --rcfile=setup.cfg **/*.py
    @echo "\n${BLUE}Running Flake8 against source and test files...${NC}\n"
    @flake8
    @echo "\n${BLUE}Running Bandit against source files...${NC}\n"
    @bandit -r --ini setup.cfg

build:
    @docker build -t ###:latest .
    @echo "\n${BLUE}Running the app...${NC}\n"
    @docker run -t ### ls -l

clean:
    rm -rf .pytest_cache .coverage .pytest_cache coverage.xml

.PHONY: clean test

docker-clean:
    @docker system prune -f --filter "label=name=$(MODULE)"
```
Change the '###' with the name of your app and you are ready to run !

## Contributors

Thanks to the following people who have contributed to this project:
@Madjakul (author)

## Contact
If you want to contact me you can reach me at [@Madjakul](https://twitter.com/madjakul).

## License
This project uses the following license: [MIT](https://github.com/Madjakul/Pynew/master/LICENSE)
