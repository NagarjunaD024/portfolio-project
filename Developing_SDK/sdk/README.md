<div align="center">

# Chapter 7 - Creating a Python SDK
![pytest](https://img.shields.io/badge/Test-pytest-%23624CAA?logo=pytest&logoColor=white)
![httpx](https://img.shields.io/badge/HTTP-httpx-%23228BE6?logo=python&logoColor=white)
![pydantic](https://img.shields.io/badge/Data-pydantic-%23E83A59?logo=python&logoColor=white)
![backoff](https://img.shields.io/badge/Retry-backoff-%237952B3?logo=python&logoColor=white)
![pyarrow](https://img.shields.io/badge/Data-pyarrow-%2350C878?logo=apachearrow&logoColor=white)
![FastAPI](https://img.shields.io/badge/API-FastAPI-teal?logo=fastapi&logoColor=white)
</div>



## Installing swcpy

To install this SDK in your environment, execute the following command:

`pip install swcpy@git+https://github.com/NagarjunaD024/
 portfolio-project#subdirectory=sdk`

## Example usage

This SDK implements all the endpoints in the SWC API, in addition to providing 
bulk downloads of the SWC fantasy data in CSV format.

### Setting base URL for the API
The SDK looks for a value of `SWC_API_BASE_URL` in the environment. The preferred 
method for setting the base URL for the SWC API is by creating a Python 
`.env` file in your project directory with the following value:

```
SWC_API_BASE_URL={"http://0.0.0.0:8000"}
```

You may also set this value as an environment variable in the environment you 
are using the SDK, or pass it as a parameter to the `SWCConfig()` method.


### Example of normal API functions

To call the SDK functions for normal API endpoints, here is an example:

```python
from swcpy import SWCClient
from swcpy import SWCConfig

config = SWCConfig(swc_base_url="http://0.0.0.0:8000",backoff=False)
client = SWCClient(config)    
leagues_response = client.list_leagues()
print(leagues_response)
```

### Example of bulk data functions

The build data endpoint returns a bytes object. Here is an example of saving 
a file locally from a bulk file endpoint:

```python
import csv
import os
from io import StringIO

config = SWCConfig()
    client = SWCClient(config)    

    """Tests bulk player download through SDK"""
    player_file = client.get_bulk_player_file()


    # Write the file to disk to verify file download
    output_file_path = data_dir + 'players_file.csv'
    with open(output_file_path, 'wb') as f:
        f.write(player_file)
```
