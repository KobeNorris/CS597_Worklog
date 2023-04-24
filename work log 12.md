#  Work Report

## Time Period

* Apr 17th 2023 - Apr 23th 2023

## Worklog (10 hours)

* Summary

* Project Details:

    * Task 1: Debug and deploy `Restler Fuzzer` on `Rest_Go` with environmental support such as path definition & library (3 Hours):
        * Download, Unzip, and Verify `dotnet 5` to Azure platfrom
        * Testify `restler fuzzer`'s functionality using cmd and sample service
        * Debug `run_tool.py` with `can not found dotnet` error
        * With Prof Darko's help, add path variable initializatin to `.bashrc` file
        * Further Debug `run_tool.py` and add path varible update code to each generated subprocess to resolve the `can not found dotnet` error

    * Task 2: Debug the six project on `REST Go` which is not running properly (7 Hours):
        * `Problem Controller`
            * Identify duplicated docker container issue, developed a purified script to clean up docker containers after ecah run
            * The problem remains, switch to GCP for replication
        * `news`
            * Debugged `set_up.sh` to properly build the `news` project
            * Testify the fix using Azure VM instance provided by Yang, and successfully generate the test coverage report
        * `ocvn`
            * Identify the `ocvn_web...jar` file unfound dependency issue
            * Built `ocvn` project locally on GCP
            * Resolved the denpendency issue
        * `Language tool`
            * Debugged `set_up.sh` for building the `Language tool` project
            * Investiagted the `spring_boot` and `failsafe` plugin documentaion to skip building these two plugin files using command line arguments