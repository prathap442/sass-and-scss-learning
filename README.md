For setting up the sass here i basically required the help of the ruby gem so
```
  gem install sass 
```
stye2.sass
this is a must


And coming to the directory structure of mainitanenance of the code 

```
  > scss
     - main.scss
  > css
     - main.css
  about.html
  index.html
  contact.html
```


I have installed the VScode extension called LiveSass CssCompiler By Dwake and then since this extension requires a dependency  that is running of the live server because when changes are compiler then it gives out seperate css file that is why



I have Made it possible by making a folder .vscode and then upgrade the settings of mine there under settings.json as 
```
{
    "liveSassCompile.settings.formats": [
        {
          "format": "expanded",
          "extensionName": ".css",
          "savePath": "~/../css/"
        }
      ]
}
```

Thanks to VScode for giving a local Scope to set the things up in the folder that is restricted to the project .