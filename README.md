# CIPY
A Continuous Integration System in Python

### Setting up the the project locally (MacOS):

#### Step 1: Install Python 3
```shell script
brew install python3
python3 --version
```

#### Step 2 : Install pip (or upgrade if already installed)
```shell script
sudo easy_install pip
sudo pip install --upgrade pip
pip -h
```

#### Step 3 : Install virtualenv (or upgrade if already installed)
```shell script
pip install virtualenv
```

or

```shell script
pip install --upgrade virtualenv
```

#### Step 4 : Create a virtual environment
```shell script
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```

Once you have finished working with this project deactivate the virtual environment
```shell script
deactivate
```

### About

The CI system will run periodically. This means if it is set up to check for changes in five-second periods, it will run tests against the most recent commit made after the five-second period. It won't test every commit made within that period of time, only the most recent one.

This project uses Git as the repository for the code that needs to be tested.

We will only run tests that are in a directory named tests within the repository.

### Components

1. Repository Observer
2. Test Job Dispatcher
3. Test Runner