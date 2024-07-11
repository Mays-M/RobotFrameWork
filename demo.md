# [Robot Framework](https://robotframework.org/)

It is an automated testing tool created by Finnish developers: Pekka Klärck, Janne Härkönen, et al. 

If you live in Finland, this tool is especially useful as many companiesher use it.

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
   
3. [Download](https://github.com/robotframework/WebDemo) the repository from GitHub . As a result you’ll get directory WebDemo-master and demoapp , docs and login_tests subdirectories:
   
   ![Extensions](https://github.com/Mays-M/Images/blob/main/webdemo.png)
   
4. Requirements for this demo are having Python, Pip, Robot Framework and SeleniumLibrary installed. This demo includes requirements.txt -file so we just need to give command:
  
   ```sh
 pip install -r requirements.txt

5. install browser and operating system specific browser drivers for all those browsers you want to use in tests:
   pip install seleniumbase

6.
