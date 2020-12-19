# Setup for SUCKS development environment

### Python Virtual Environment

*More information [here](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)*

- Setup virtual environment

        cd <GIT_DEV_DIR>
        python3 -m venv env

- Start virtual environment
    - `source env/bin/activate`
- Confirm virtual environment started
    - `which python3` - *Output should be similar to the following:*

            ycqin@LTM1-YCQIN.local [~/personal/ecovacs/sucks]
            -> which python3
            /usr/bin/python3
            ycqin@LTM1-YCQIN.local [~/personal/ecovacs/sucks]
            -> source env/bin/activate
            (env) ycqin@LTM1-YCQIN.local [~/personal/ecovacs/sucks]
            -> which python3
            /Users/ycqin/personal/ecovacs/sucks/env/bin/python3

- Install SUCKS
    - `pip install sucks`
- Stop virtual environment
    - `deactivate`

### SUCKS library API

- Setup configuration
    - `sucks login` - *Enter `na` or `ww` for "continent code"*
    - `sucks clean 10`

### SUCKS development

- Start python virtual environment as described [above](#python-virtual-environment)
- Install development environment in [editable mode](https://stackoverflow.com/questions/35064426/when-would-the-e-editable-option-be-useful-with-pip-install)
    - `cd <SUCKS_GIT_DEV_DIR>`
    - `pip install -e .`
- Run unit tests
    - Install nose module: `pip install nose`
    - Run the tests: `nosetests`
- If the following error happens run this command: `pip install requests-mock`

        ERROR: Failure: ModuleNotFoundError (No module named 'requests_mock')
