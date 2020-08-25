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


The next step lies in declaring and utilising the variables and the variables can be utilised by 

```
/* declaring the variable*/
$text-ptag-color: #3333

/* utilising the variable in the text-color attribute */
p {
  text-color: $text-ptag-color;  
}
```

-------------
What are Partials?

The partials in the SCSS files are the files where the variables that are being declared and these are not compiled to the CSS 

The file name of the partial would start with "_"
and the partial can be imported to the main file by using the 
```
@import "./partial";

```
The above command would import an scss file by the name _partial.scss into the style.scss 


What are the Mixins in SCSS?
   The Mixins are the slots for providing the reusable pieces of the code and this reusable pieces can be reutilised at the places of the requirement .

```
  @mixin warning {
    border: 1px solid black;  
  }

  /* the below line would generate the color of the button to have the text-color to be white and then the css stylings of the border 1px and the solid black since the include  is being done by defiing the mixin above 
  */
  button {
    @include warning
    text-color: white;
  }
```


We can reutilise a mixin into another one by using the following mixin




@mixin warning {
  "border": 1px solid black;
}

@mixin danger {
  @include warning;
  "text-color": white;  
}

We can reutilise one mixin inside another mixin by using the following things.
