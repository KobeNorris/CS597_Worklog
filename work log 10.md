#  Work Report

## Time Period

* Apr 3rd 2023 - Apr 9th 2023

## Worklog (15 hours)

* Summary

* Project Details:

    * Task 1: Integrated ChatGTP into `resulter fuzzer` [replace the json data within request body with the one generated by ChatGTP] (3 Hours 30 Mins):
        * Extract and analyze `request_data`'s object structure and convert json package within into String object
        * Used the authentication token from Suraj to send request to OpenAI apis to generated more reasonable json values.

    * Task 2: Investigated `Rest_GO` testing benchmark and try to deploy it (5 Hours 30 Mins):
        * Because the codebase asks for linux libaries' supports, I created a Google Cloud Platform account and allocated a virtual machine according to the repo's requirements.
        * Debugged and deployed the `Rest_GO` project successfully on virtual machine, set up the cooresponding envrionment and run the `run_small.py` file and generate the result report using `small_report.py`. 

    * Task 3: Further investigated all tools from `Rest_GO` testing benchmark (6 Hours):
        * Tests all tools using the default project provided in `Rest_GO`, which is the `project-tracking-system`.
            * `Restler` reports bugs
            * `Schemathesis` reports bugs
            * The others seems to work fine