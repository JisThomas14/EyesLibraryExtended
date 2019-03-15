# EyesLibrary for Robot Framework

## Introduction

EyesLibrary is a Robot Framework Library to automate visual software testing verification. EyesLibrary uses a Python SDK called [Eyes-Selenium](https://pypi.python.org/pypi/eyes-selenium) from the tool [Applitools Eyes](http://applitools.com/), and can be used with the [SeleniumLibrary](https://github.com/robotframework/SeleniumLibrary) and/or the [AppiumLibrary](https://github.com/serhatbolsu/robotframework-appiumlibrary) .

This library is a fork of [Robot-AppEyes](https://github.com/NaviNet/Robot-AppEyes).
In order to use EyesLibrary, you are required to [sign up](https://applitools.com/sign-up/) for a free account with Applitools. See the [Usage](https://github.com/joel-oliveira/EyesLibrary#usage) section.

- Information about EyesLibrary keywords can be found on the [Keyword Documentation](https://joel-oliveira.github.io/EyesLibrary/) page.

- The [Eyes Selenium](https://pypi.org/project/eyes-selenium/) page provides more information for that library.
- More information about the SeleniumLibrary can be found on the [SeleniumLibrary Repo](https://github.com/robotframework/SeleniumLibrary) and in the [Keyword Documentation](http://robotframework.org/SeleniumLibrary/SeleniumLibrary.html).
- More information about the AppiumLibrary can be found on the [AppiumLibrary Repo](https://github.com/serhatbolsu/robotframework-appiumlibrary) and in the [Keyword Documentation](http://serhatbolsu.github.io/robotframework-appiumlibrary/AppiumLibrary.html).

## Requirements

- Python 2.7.14
- Robot Framework 3.1.1
- Eyes-Selenium 3.15.2
- SeleniumLibrary 3.3.1 (For Web Tests)
- AppiumLibrary 1.5.0.2 (For Mobile Tests)

## Installation

This library is not ready yet for installation.

<!--
#### Using pip

The recommended installation tool is [pip](http://pip-installer.org).

Install pip.
Enter the following:

    pip install Robot-AppEyes

Append `--upgrade` to update both the library and all
its dependencies to the latest version:

    pip install --upgrade Robot-AppEyes

To install a specific version enter:

    pip install Robot-AppEyes==(DesiredVersion)

#### Manual Installation

It is also possible to install the package with python, though you will need dependencies to be installed manually.
you can download the source distribution from PyPI, extract it and
run the following command:

    python setup.py install

Alternatively you could download the source code, package it and install using next commands:

        python setup.py sdist
        pip install resulting_package
        ## dist/robot-appEyes-1.2.zip

#### Uninstall

To uninstall Robot-AppEyes use the following pip command:

    pip uninstall Robot-AppEyes

However, if the package was installed manually it will need to be uninstalled manually:

1. Navigate to `C:\Python27\Tests` and delete RobotAppEyesTest.txt, pictureOne.png, pictureTwo.png and RobotAppEyes-KeywordDocumentation.html

2. Navigate to `C:\Python27\Lib\site-packages` and delete RobotAppEyes-1.2-py2.7.egg-info and the folder `RobotAppEyes`

## Directory Layout

_EyesLibrary/EyesLibrary.py_ :
The Robot Python Library that makes use of the Applitools Eyes Python SDK.

_Tests/acceptance/EyesLibraryTest.txt_ :
Example test file to display what various keywords from EyesLibrary Library accomplish

_doc/EyesLibrary-KeywordDocumentation.html_ :
Keyword documentation for the EyesLibrary library.
 -->

## Usage

To write tests with Robot Framework and EyesLibrary,
EyesLibrary must be imported into your Robot test suite.
See [Robot Framework User Guide](http://code.google.com/p/robotframework/wiki/UserGuide) for more information.

**Note** - You must create a [free account](https://applitools.com/sign-up/) with Applitools in order to run the
EyesLibrary and return results. The Applitools site will
allow you to sign up and you will then be provide with your own API key.
This will then need to be added to the Robot test file EyesLibraryTest.robot,
within the variable \${Applitools-Key}, remove 'YourApplitoolsKey' and replace with your API Key.

## Running the Demo

At _tests/acceptance_ directory, you can find Robot Framework tests for:

- Web
- Android Browser
- Android Native App
- Android Hybrid App
- iOS Browser
- iOS Native App
- iOS Hybrid App

Before running the tests, your Applitools Api Key must be set in _tests/acceptance/resources/common.robot_, by replacing "YourApplitoolsApiKey" with your own key.

When running the mobile tests, you must replace the variables within _tests/acceptance/resources/mobile.robot_ with your own, as well as the ones in _tests/acceptance/resources/android.robot_ or _tests/acceptance/resources/ios.robot_, according to the OS in use.

Before running the Mobile Hybrid App tests, you need to install the Demo App (APK found at _tests/resources_) in your device.

For in depth detail on how the keywords function, read the Keyword documentation found here : [Keyword Documentation](https://joel-oliveira.github.io/EyesLibrary/)

**Remember to include your Applitools API key otherwise the
test will not run.** To run a test, open a command prompt within the _tests/acceptance_ folder and run:

    robot FILENAME.robot

For example, to run the Test Suite for Web:

    robot web.robot

**Note:** It is assumed that anyone who wants to use this demo script is already able to execute robot tests using Google Chrome.

## Things to Note When Using Applitools

- The tests will be accepted automatically by Applitools Eyes after the first run because a new baseline is being created. A second test run will show a successful comparison between screens.
- Changing the Applitools' Application Name variable value will create a new test entry in Applitools test result screen and a new baseline will be accepted automatically by Applitools Eyes on the first run.
- The viewport size should not be set to greater values than the maximum size of the device's window. (For more information on using viewports, https://applitools.com/docs/topics/general-concepts/using-viewports-in-eyes.html)

## Getting Help

To be defined.
