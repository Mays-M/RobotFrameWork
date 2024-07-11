# [Robot Framework](https://robotframework.org/)

It is an automated testing tool created by Finnish developers: Pekka Klärck, Janne Härkönen, et al. 

If you live in Finland, this tool is especially useful as many companiesher use it.

## How to Test Your Work:

### Web testing with Robot Framework and SeleniumLibrary

1. Install Python: [Download Python](https://www.python.org/downloads/)

2. On Windows, navigate to **cmd** and type:

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

4. In Visual Studio Code, install the Robot Framework extension
   
   ![Extensions](https://github.com/Mays-M/Images/blob/main/extensions.png)
   
6. Create a Test File: Create a file named for exmaple **test.robot** with the following content:
  
  ```sh
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

    
6. Run the Test:

In the terminal, run the following command: robot test.robot
