# [Robot Framework](https://robotframework.org/)

It is an automated testing tool created by Finnish developers: Pekka Klärck, Janne Härkönen, et al. If you live in Finland, this tool is especially useful as many companies there use it.

## How to Test Your Work:

### Get Started with Installation:

1. Install Python: [Download Python](https://www.python.org/downloads/)

2. On Windows, navigate to cmd and type:

   ```sh
   # To verify that Python is installed
   python --version

   # To install Robot Framework
   pip install robotframework

   # To verify that Robot Framework is installed
   robot --version

   # To install the Selenium library
   pip install robotframework-selenium2library

   # To check the library list
   pip list
   
3. Install Visual Studio Code

4. In Visual Studio Code, install the Robot Framework extension (link to picture)

Create a Test File:
Create a file named test.robot with the following content:

"""
*** Settings ***
Library           SeleniumLibrary  # Updated to SeleniumLibrary, as Selenium2Library is deprecated

*** Variables ***
${BROWSER}        Google Chrome
${URL}            http://www.google.com

*** Test Cases ***
Go to Google
    [Documentation]    Open Google in a browser
    Open Browser    ${URL}    ${BROWSER}
    [Teardown]    Close Browser

Google Index
    [Documentation]    Open Google in a browser
    Open Browser    ${URL}    ${BROWSER}
    [Teardown]    Close Browser
"""

markdown
Copy code
# [Robot Framework](https://robotframework.org/)

It is an automated testing tool created by Finnish developers: Pekka Klärck, Janne Härkönen, et al. If you live in Finland, this tool is especially useful as many companies there use it.

## How to Test Your Work:

### Get Started with Installation:

1. Install Python: [Download Python](https://www.python.org/downloads/)

2. On Windows, navigate to cmd and type:

   ```sh
   # To verify that Python is installed
   python --version

   # To install Robot Framework
   pip install robotframework

   # To verify that Robot Framework is installed
   robot --version

   # To install the Selenium library
   pip install robotframework-selenium2library

   # To check the library list
   pip list
Install Visual Studio Code

In Visual Studio Code, install the Robot Framework extension (link to picture)

Create a Test File:
Create a file named test.robot with the following content:

robot
Copy code
*** Settings ***
Library           SeleniumLibrary  # Updated to SeleniumLibrary, as Selenium2Library is deprecated

*** Variables ***
${BROWSER}        Google Chrome
${URL}            http://www.google.com

*** Test Cases ***
Go to Google
    [Documentation]    Open Google in a browser
    Open Browser    ${URL}    ${BROWSER}
    [Teardown]    Close Browser

Google Index
    [Documentation]    Open Google in a browser
    Open Browser    ${URL}    ${BROWSER}
    [Teardown]    Close Browser
Run the Test:

In the terminal, run the following command: robot test.robot
