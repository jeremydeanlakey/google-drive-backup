Google Drive Backup
===================

A python script to incrementally backup your google drive contents.

## Features
* You can Download your entire google drive or any given folder
* Downloads a file only if it has been modified since last download
* Zips file to reduce disk space
* Keeps copies of previously downloaded versions
* Logs all actions (optional)
* Uses OAuth2 authentication and can remember authentication
* List backup copies of a specific file or folder

## Requirements
* Google API Python library. To install run
`pip install --upgrade google-api-python-client` or
`easy_install --upgrade google-api-python-client`
* sqlite3
`pip install --upgrade sqlite3`

## Setup
* Edit `client_secrets_sample.json` and add your Google API client id and client secret (If you don't have one, [get it here](https://code.google.com/apis/console/)).
* Save it as `client_secrets.json`.
* Now, if you run `python backup.py`, a browser window/tab will open for you to authenticate the script.
* Once authentication is done, the script will start downloading your *My Drive*. Refer the next section for more options.

## Options for backup.py
Following command line options are available.

**--destination** - Path to the folder where the files have to be downloaded to. If not specified, a folder named `downloaded` is created in the current directory.

**--debug** - If present (accepts no value), every step will be logged to the log file.

**--logfile** - Path to the file to which the logs should be written to. By default, writes to `backup.log` in the current directory. The file will be overwritten every time the script is run.

**--drive_id** ID of the folder which you want to download. By default, entire "My Drive" is downloaded.

## Options for recover.py
Following command line options are available.

**--destination** - Path to the folder where the files were downloaded to. If not specified, a folder named `downloaded` is used.

**--file_id** ID of the file which you want to recover.

**--file_name** Exact file name of the file you want to recover.

**--folder** Exact name of the folder you want to recover.



