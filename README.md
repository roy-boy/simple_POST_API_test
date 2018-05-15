# simple_POST_API_test
a data driven test automation harness writen in Python to verify http endpoint

project structure:
API_test/ project directory contains Python code for execution and sub-dir, run_api_test.py is the program entry script to execute test 
API_test/test_input/ – test input data required for test execution, test case CSV files lives here
API_test/test_output/ – test output directory contains test_result_ouput.csv and test harness log file

How to setup your test exeution environment:
1. if on Windows, install Python version 2.7.6+ from https://www.python.org/downloads/windows/
2. if on Linux, it should have Python insatlled with OS, just check from console '$python --version'. If not installed try 'sudo apt-get install python2.7'
3. once Python is installed on your OS, insall HTTP library dependency 'requests' for POST HTTP request
    on Windows CMD: run 'python pip install requests' then run upgrade package 'python pip install --upgrade requests'
    on Linux: run '$sudo python pip install requests' then run upgrade package '$sudo python pip install --upgrade requests'

How execute test:
1. first to check the test input data csv file in API_test/test_input/ check which test case is set to 'Y' to be executed, each row is a test scenario with the payload to be posted
2. second open \API_test\test_config.py via text editor to confirm the POST URL is pointing to the target endpoint
3. then in your CMD console go to \API_test\, run 'python run_api_test.py' 
4. after test execute done, there is console raw out put also the test log file for debugging
5. the test result is captured in API_test/test_output/test_result_ouput.csv, the column 'TEST_RESULT' holds the 'Passed' or 'Failed'
