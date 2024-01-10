This is connected to github

# BEFORE ANYTHING
Read the whole page. It will help you to understand the rest of this doc
https://github.com/robocorp/rpaframework/blob/master/docs/source/contributing/development.md


# To Build
## One time Setup
1. Have Python  3.9.16 installed : `pip install poetry==1.6.1`
2. Install Poetry //TODO who did I install it?
3. Install Invoke:  //TODO was `pip install invoke` ?

### Installing requirements
Now you are good to go with running these installation commands once from the root dir:

```
python -m pip install -Ur invocations/requirements.txt

inv install.install-local
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

# What I did
I followed the installation from Developers Guide and stopped at `PyPI & DevPI` (without doing it)
https://github.com/robocorp/rpaframework/blob/master/docs/source/contributing/development.md#pypi--devpi


## Commands
## Remove docutils dependenci
         poetry remove docutils