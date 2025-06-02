# Coolify Cronicle + FileBrowser

thanks to
- https://github.com/soulteary/docker-cronicle/
- https://github.com/jhuckaby/Cronicle
- https://github.com/flavsdotpy/docker-cronicle-python


Default account and password:

- username: `admin`
- password: `admin`



## Adding a new Python script to run

* Copy your python script to `$HOME/.cronicle/scripts/python`
* Open [Cronicle console](localhost:3012)
* Go to `Schedule > [+] Add event...`
* Create the job as:
  * Plugin: `Python Script`.
  * Script path: the path to your script file, relative to `scripts/python` (i.e. `my_script.py` for `$HOME/.cronicle/scripts/python/my_script.py`).
  * Required packages (not required): the same content of your `requirements.txt` file, each package in a line (with `==<version>` if needed).
  * Environment variables (not required): environment variables, one per line, in the format of a .env file (i.e. `AWS_REGION=us-east-1`)
  * Parameters (not required): single string of script parameters (i.e. `--v -f file.txt`)

For all other configurations, please refer to [cronicle official docs](https://github.com/jhuckaby/Cronicle/blob/master/docs/WebUI.md).
