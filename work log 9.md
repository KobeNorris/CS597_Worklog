#  Work Report

## Time Period

* Mar 27th 2023 - Apr 2th 2023

## Worklog (14 hours)

* Summary

* Project Details:

    * Task 1: Instrumentalize `LakesideMutual` Controller files (7 Hours):
        * Add `sl4j` dependencies to build.gradle file
            * `customer-core\pom.xml`
            * `customer-self-service-backend\pom.xml`
            * `policy-management-backend\pom.xml`
        * Configure the ``sl4j`` logging settings to define the logging level and output format
        * Add `sl4j` loggers to the controller files to log events and actions
            * `customer-core`
                * `customer-core\src\main\java\com\lakesidemutual\customercore\interfaces\CustomerInformationHolder.java`
            * `customer-self-service-backend`
                * `customer-self-service-backend\src\main\java\com\lakesidemutual\customerselfservice\interfaces\AuthenticationController.java`
                * `customer-self-service-backend\src\main\java\com\lakesidemutual\customerselfservice\interfaces\CustomerInformationHolder.java`
                * `customer-self-service-backend\src\main\java\com\lakesidemutual\customerselfservice\interfaces\InsuranceQuoteRequestCoordinator.java`
            * `policy-management-backend`
                * `policy-management-backend\src\main\java\com\lakesidemutual\policymanagement\interfaces\PolicyInformationHolder.java`
                * `policy-management-backend\src\main\java\com\lakesidemutual\policymanagement\interfaces\RiskComputationService.java`
        * Rewrite the request mapping interface in controller files to grab all incoming `POST` requests' `JSON` parameters
        * Test and verify the output loggings
            * Failed with Suraj's submodule project
                * `https://github.com/Suraj-Vashista-BK/LakesideMutual/tree/f0710fbe6e96442739169a894673b9263d95c180`
                * Compose Failed - `Port 61613 is Occupied`
            * Failed with Akshathsk's project
                * `https://github.com/akshathsk/LakesideMutual`
                * Build Failed - `Dependency unresolved`

    * Task 2: Investigating `resulter fuzzer` codebase [Find request sender] (4 Hours 30 Mins):
        * Try to continue searching through `driver.py` and `request.py`
            * Read thourgh `request.py`
            * Read through all schema realtive files, find `checker_base.py` to be the request sender.
        * Try to continue searching through `checker_base.py`:
            * Read through target file, find `_send_request` to be the request sender function.
            * Within `_send_request`, find the `request_utilities.send_request_data` has been called
        * Verify that the result by logging all the requests sending out.

    * Task 3: Investigating `dependency.json` (2 Hours 30 Mins):
        * Analyzed the `grammar.py`, `dependencies.json`, `unsolved_dependencies.json`, and `dependencies_debug.json`
        * Found that the resulter fuzzer read through the swagger file and try to work out the dependencies of single attributes of the object send in the requests
            * Not applicable
            * Targeting end points not exist
            * Verified by self defined swagger file