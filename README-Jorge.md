This is connected to github

# BEFORE ANYTHING
Read the whole page. It will help you to understand the rest of this doc
https://github.com/robocorp/rpaframework/blob/master/docs/source/contributing/development.md


# To Build
## One time Setup
1. Have Python  3.9.16 installed : 
2. Install Poetry //TODO who did I install it? `pip install poetry==1.6.1`
3. Install Invoke:  //TODO was `pip install invoke` ?

### Installing requirements
Now you are good to go with running these installation commands once from the root dir:

```
python -m pip install -Ur invocations/requirements.txt

inv install.install
```
### Building the Poetry venv for the first time in the main package:
```
cd packages/main
inv install
```

### Now run the unit tests to ensure you are good so far
```
cd packages/main
inv code.test-python
```
## To run a Robot
```
cd .env
poetry shell

cd <robot directory>  #e.g. /Users/jherreri/Documents/RobotExamples/OPEN_SOURCE_APPROVAL_OPEN_GOOGLE_1.00.00
python -m robot -d ./output transpiled_tasks.robot
```


# What I did
I followed the installation from Developers Guide and stopped at `PyPI & DevPI` (without doing it)
https://github.com/robocorp/rpaframework/blob/master/docs/source/contributing/development.md#pypi--devpi


## Commands
### Remove docutils dependency
         poetry remove docutils