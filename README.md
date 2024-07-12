# [Robot Framework](https://robotframework.org/)

Robot Framework is released under the Apache License 2.0. Development of Robot Framework is sponsored by the Robot Framework Foundation. The basis for Robot Framework is Pekka Klärck’s Master’s thesis for Helsinki University of Technology in 2006.

If you live in Finland, this tool is especially useful as many finnish companies use it.

### Keywords

- Keywords are like functions that you execute to accomplish various tests.
- Keywords can be reused and composed, which means that you create keywords by calling other keywords
  
  #### Library keywords
  
- Library keywords are the lowest level building blocks of creating user keywords and using them in test cases.
- Libraries are normally imported in the Settings section but can also be imported in the Test Cases section using the Import Library keyword from the BuiltIn Library
  
### Defining variables

- Variables, as keywords, are case-insensitive, and spaces and underscores are ignored.
- Recommendation is to use CAPITAL letters with global variables like ${PATH} and small letters with local variables like ${name}.
- Variable names have type identifiers and variable names between the mandatory curly braces like ${VAR}.
- Robot Framework has scalars ${SCALAR}, lists @{LIST} and dictionaries &{DICT}. Environment variables are used as strings with %{ENV_VAR}.

  
## Web testing with Robot Framework and SeleniumLibrary

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
   
3. Download [Web Testing Demo](https://github.com/robotframework/WebDemo) the repository from GitHub . As a result you’ll get directory WebDemo-master and demoapp , docs and login_tests subdirectories:
   
   ![web_Demo](https://github.com/Mays-M/Images/blob/main/webdemo.png)
   
4. Requirements for this demo are having Python, Pip, Robot Framework and SeleniumLibrary installed. This demo includes requirements.txt -file so we just need to give command:
    ```sh
     pip install -r requirements.txt

6. install browser and operating system specific browser drivers for all those browsers you want to use in tests:
   pip install seleniumbase

 7. Next we start the demo application with command:
    <h3>Manually testing </h3>

    ```sh
      python demoapp/server.py

![Extensions](https://github.com/Mays-M/Images/blob/main/manual_test.png)

Open browserand navigate to http://localhost:7272 .

The demo application is a very simple login page. With user name demo and password mode you get into a welcome page and otherwise you end up on an error page.

Now try to login to manually test, end the server by pressing ctrl-c.


![Extensions](https://github.com/Mays-M/Images/blob/main/login_page.png)

<h3>Automated test using robot</h3> 

- so let’s start it again.
- Locate demoapp/server.py from your file manager and Run it with python
- next run automated tests with cmd:
     ```sh
      robot login_tests
     
![Extensions](https://github.com/Mays-M/Images/blob/main/pass_report.png)
  

## Result of the Test

<h4>Report.html</h4>

![Extensions](https://github.com/Mays-M/Images/blob/main/report_html.png)


<h4>log.html</h4>

![Extensions](https://github.com/Mays-M/Images/blob/main/log_html.png)






