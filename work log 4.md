#  Work Report

## Time Period

* Feb 20th 2023 -  Feb 26th 2023

## Worklog (14 hours 30 Mins)

* Summary

* Project Details:

    * Offline Meeting with Professors:

        * Time Spent: 1 Hour 30 Mins
        * Date: Feb 20th 12:00 - 1:30
        * Description: Review last week progress this week task.
            * Last Week Task: 
                * Generation 10 tests for current project (`robot-shop`): Generated 5 test workflow with 12 tests in total.
            * This Week Task:
                * Generate more tests for current project (`robot-shop`), based on more complicated workflow
                * Enable project (`robot-shop`) to be built and deployed from local source code
                * Further develop the project (`robot-shop`) to enable users to deploy it easily using command line on linux OS. 
                * Prepare for Wednesday demo to IBM founders

    * Merge PR for last week

        * Time Spent: 1 Hour
        * Date: Feb 20th 3:30 - 4:30
        * Description:
            * Further improve the readme file
            * Create and Integrate `submodule` for project with specific branch
            * Merge PR with `rebase` and `squash`

    * Generate more tests based on more complicated workflow

        * Time Spent: 2 Hours 30 Mins
        * Date: Feb 20th 6:00 - 8:30
        * Description:
            * Refine old tests' assertations using more detailed expected content
            * Remove tests which are overly simple
            * Generate 6 tests based on more complicated workflow

    * Enable project to be built and deployed from local source code:

        * Time Spent: 7 Hours
        * Date: Feb 21th 6:00 - 9:30 + 10:30 - 2:00
        * Description:
            * Debug original dockerfiles and local shell scripts
                * Because windows use CRFL format (instead of FL), direct copy scripts to container will crash the system
                * The debug information is vague and useless, discussed with Akshath and David, but solved individually
            * Refined and further developed the build and deploy instructions
            * Test all other paticipants' project using window system with each integration codebase
            * Discussed and try to debug the docker hub manifest lost problem on Mac (with Akshath, Suraj, and Chimay)

    * Review and setup backup system for Akshath's presentation:

        * Time Spent: 2 Hour
        * Date: Feb 22th 9:00 - 10:00 + 12:00 - 1:00
        * Description: 
            * Refined the readme and tests according to David's and Akshath's suggestions
            * Provide back up support for Akshath's presentation

    * Discussed and Assigned codeQL task for the rest of the week:

        * Time Spent: 30 Mins
        * Date: Feb 23th 7:00 - 7:30
        * Description: 
            * Discussed and Assigned codeQL task for the rest of the week: