
This is a simple & minimal guide on how to use the google-sheet service with Python.

## Requierements

Let's start by defining the system requirements and installing the dependencies.

System requirements:
* Python 3.5 or greater

Dependencies:
* `google-api-python-client==1.8.3` 
* (optional) `jupyter==1.0.0`

```commandline
$ pip install google-api-python-client==1.8.3 jupyter==1.0.0
```

## Enable the Google Speadsheet API

Create a Google Cloud project (https://console.cloud.google.com/) and enable the Google Sheets API.

![](https://hackmd.io/_uploads/S1LAtHDI5.png)

Next step is to create an API Key. Using this key is the fastest way to get going.

![](https://hackmd.io/_uploads/BkN9k8vIq.png)

## Python Code!

Let's start with the imports, configuration variables, and singeltons:


```python 
import os
from googleapiclient import discovery

# Get the key from the environ variables
SHEETS_API_KEY = os.environ.get(
    "SHEETS_API_KEY",
    default="YOUR-KEY"  # TODO: Replace with your testing key here
) 

# Create the API Service instance
service = discovery.build(
    "sheets",
    "v4",
    developerKey=SHEETS_API_KEY
)

speadsheet_values = service.spreadsheets().values()
```

![](https://hackmd.io/_uploads/HJ8DwUwIc.png)


We should now be able to get the data from a Google Speadsheet!

Consider the following google sheet:
* Sheet URL: [here](https://docs.google.com/spreadsheets/d/1uFMvhLcLxVDeFxBw8Zt5cIuVKc_h0ByqLDx2kWlNXOY/)
* Sheet Name: `example`
* Sheet ID: `1uFMvhLcLxVDeFxBw8Zt5cIuVKc_h0ByqLDx2kWlNXOY`

We should be able to get the data:

```python=
spreadsheet_id = "1uFMvhLcLxVDeFxBw8Zt5cIuVKc_h0ByqLDx2kWlNXOY"
spreadsheet_range = "A1:B4"


request = spreadsheet_values.get(
    spreadsheet_id=spreadsheet_id,
    range=spreadsheet_range,
)

response = request.execute()
```
![](https://hackmd.io/_uploads/ry7FP8vL9.png)

If we add `pandas` to our requirements, we should be able to easily transform the results into a DataFrame.

![](https://hackmd.io/_uploads/rkoMuIPIq.png)
