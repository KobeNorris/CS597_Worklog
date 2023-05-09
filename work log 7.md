#  Work Report

## Time Period

* Mar 13th 2023 - Mar 19th 2023

## Worklog (9 hours 30 mins)

* Summary

* Project Details:

    * Online Meeting with Professors:

        * Time Spent: 1 Hour 30 Mins
        * Date: Mar 13th 12:00 - 1:30
        * Description: Review last week progress

        
    * Investigate how Restler Fuzzer generate param combinations (2 Hours):

        * Try to get the calling stack path of `param_combinations.py` to obtain the param generator

            1. `restler\engine\fuzzing_parameters\param_combinations.py`
                * 16 - `get_param_list_combinations`
                    * Param - `param_list`
                * 76 - `get_param_combinations`
                    * Param - `param_list`
            
            2. `restler\engine\core\requests.py`

                * 1391 - `get_query_param_combinations`
                    * Param - `self.headers_schema.param_list`
                * 1491 - `get_header_param_combinations`
                    * Param - `self.headers_schema.param_list`
                * 783 - `get_all_example_schemas`
                    * No caller

        * Try to get the calling stack path of `param_combinations.py` to obtain the param generator (3 Hours):

            1. Deploy `ftgo-application` locally on Windows
                * `.NET 6.0` is incompatible with windows processor
                    * Switch to `.NET 7.0`
            
            2. The Logger has not print any thing using three fuzzing testing modes
                * RESTler in test mode
                * Fuzzing with fuzz-lean mode
                * Fuzzing with fuzz mode
                * Seems that all relative functions have not been called

        * Try to trace the call path starting from the init of function （3 Hours）:

            1. Test Fuzzing Lean:
                * `./restler_bin/restler/Restler fuzz-lean --grammar_file ./Compile/grammar.py --dictionary_file ./Compile/dict.json --settings ./Compile/engine_settings.json --no_ssl`

            1. Test Fuzzing:
                * `./restler_bin/restler/Restler fuzz --grammar_file ./Compile/grammar.py --dictionary_file ./Compile/dict.json --settings ./Compile/engine_settings.json --no_ssl --time_budget 1`