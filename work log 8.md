#  Work Report

## Time Period

* Mar 20th 2023 - Mar 26th 2023

## Worklog (12 hours 30 mins)

* Summary

* Project Details:

    * Online Meeting with Professors:

        * Time Spent: 1 Hour 30 Mins
        * Date: Mar 20th 12:00 - 1:30
        * Description: Review last week progress, and assign this week tasks:
            1. Instrumentalize Controller files of `ftgo-application` to collect and log all request information;
            2. Continue investigating the `resulter fuzzer` code base, to find out where does the codebase generate `JSON` parameters;
            3. Investigating the `dependency.json` file to see, whether filling this file could promote test coverage.

    * Task 1: Instrumentalize `ftgo-application` Controller files (5 Hours):

        * Add `sl4j` dependencies to build.gradle file
        * Add `sl4j` loggers to the controller files (`ftgo-consumer-service\src\main\java\net\chrisrichardson\ftgo\consumerservice\web\ConsumerController.java`) to log events and actions
        * Configure the ``sl4j`` logging settings (`ftgo-consumer-service\src\main\java\net\chrisrichardson\ftgo\consumerservice\web\ConsumerController.java`) to define the logging level and output format
        * Rewrite the request mapping interface in controller files to grab all incoming `POST` requests' `JSON` parameters
        * Test and verify the output loggings

    * Task 2: Investigating `resulter fuzzer` codebase (6 Hours):

        * Try to continue searching through `restler.py` and `request.py`
            * Read thourgh `request.py`
            * Read through all schema realtive files, find `__add__` operation to add requests
        * Try to continue searching through all files under `Compiled` folder:
            * From log files, search for `Rendering INVALID`
            * From log files, search for `restler_static_string`
            * Investigate grammar relative generated files
        * Try to search for `primitive.py`

    * Task 3: Investigating `dependency.json`:

        * 