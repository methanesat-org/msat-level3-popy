# Golden Test Data

## Overview

This directory contains the inputs and expected outputs in order to determine that everything works as expected when changing pulling in the latest version of the L2-L3 code.

## How to run

#TODO: ## Automate the running of these tests

Run the following steps from the root directory of this github repo

1. conda activate level3
2. Run the pythyon

    ```
    python3 msat_l3.py -i testdata/golden/input -o /tmp --start-time 2016-10-01 --end-time 2016-10-30 -w -100 -e -95 -n 35 -s 30 --grid-size 0.001
    ```

3. Make sure there are no unexpected errors or warnings.
4. Diff the outputs.

    ```
    diff /tmp/l3.png testdata/golden/output/l3.png
    ```
