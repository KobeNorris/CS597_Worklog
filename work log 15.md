#  Work Report

## Time Period

* May 8th 2023 - May 14th 2023

## Worklog (9 Hours)

* Summary

* Project Details:

    * Task 1: Online Meeting with Professors (2 Hours):

        * Review last week progress and assign this week's task.

    * Task 2: Generate `enum_extraction.sh` script which automatically extract `Enums` from 19 projects of `REST_Go` (7 Hours)
        * Generate a Bash script to extract `Enums` from 19 projects of `REST_Go`, which is of high flexibility and robustness.
        * Verified the results generated from the `enum_extraction.sh` to the results from bash commmand of all 19 project.
        * As `codeql` works during project compilation, `Enums` from `Gradle` project `erc20` could hardly be extacted, therefore, only 19 projects could be generated.
        * Updated the `enum_extraction.sh` to be able to convert the results from `codeql` to `UIUC-API-Tester`'s inputing `JSON` file format.
        * Developed full Doc for `enum_extraction.sh` and created the PR to both Akthash's personal repo and Organiztion's repo.