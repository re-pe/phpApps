# Modified PHP Desktop

There is file with modified function which PHP Desktop uses for loading of settings.json file. 

Modifications lets PHP Desktop to load chain of json files until it finds branch named *Desktop*. 

Search begins from file start.conf in folder where phpdesktop-chrome.exe is placed. If *Desktop* branch is not found, branch with name *Settings* is searched, and new settings file path/conf is loaded.

start.conf:
```javascript
{
    "Settings" : {
        "Path" : "_defaults",
        "Conf" : "app.1.conf"
    }
}
```

_defaults/app.1.conf:
```javascript
{
    "Desktop" : {
        "Path" : "_defaults",
        "Conf" : "settings.json"
    }
}
```

## Usage

Download source of PHP Desktop Chrome 47.5, replace settings.cpp with this file and compile phpdesktop according instructions on PHP Desktop site. If you want to get binary file, download it [here](https://drive.google.com/open?id=0BxuT8ypXm7sRalNNQU1jdDJvSlU).
