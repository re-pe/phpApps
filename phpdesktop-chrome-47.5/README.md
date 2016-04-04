#Modified PHP Desktop

There is file with modified function which PHP Desktop uses for loading of settings.json file. 

Modifications lets PHP Desktop to load chain of json files until it finds branch named "Desktop". 

Search begins from file start.conf in folder where phpdesktop-chrome.exe is placed. If Desktop branch is not found, branch with name Settings is searched, and new settings file path/conf is loaded.

```{
	"Settings" : {
		"Path" : "_defaults",
		"Conf" : "app.1.conf"
	}
}```

```{
	"Desktop" : {
		"Path" : "_defaults",
		"Conf" : "pd.conf"
	}
}```


Download source of PHP Desktop Chrome 47.5, replace settings.cpp with this file and compile phpdesktop according instructions on PHP Desktop site.