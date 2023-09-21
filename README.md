# Stadium Theming-Kit
A set of CSS variables that allow for extensively changing the look and feel of Stadium applications without writing any CSS

## Contents
The kit consists of a number of separate, but related CSS files. 
1. *theming-variables.css* contains a set of variables (the only file you need to make changes to)
2. *theming.css* contains CSS instructions to apply the variables
3. *theming-fallbacks-default-theme.css* contains the fallback variables for the Stadium default theme (Material Design Blue)
4. *theming-fallbacks-grey-theme.css* contains the fallback variables for the Grey theme

## Customisations
To customise a theme using this kit
1. Uncomment attributes to be customised in the *theming-variables.css* file
2. Amend the related values as you see fit

## Implementation

### Stadium 6 (versions 6.6 and above)
1. Add three CSS files to the Embedded Files of your application
   1. Your customised *theming-variables.css* file
   2. The *theming.css* as is
   3. The fallback values file
      1. The *theming-fallbacks-default-theme.css* file if your Stadium Theme is *Default*, *PinkBlue*, *Purple* or *Teal*
      2. The *theming-fallbacks-grey-theme.css* file if your theme is *Cobalt*, *Dark*, *DarkRed*, *Forest*, *Grey*, *Orange* or *Scarlet*
2. Paste the link tags below into the *Head* property of your application
```
<link rel="stylesheet" href="{EmbeddedFiles}/theming.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theming-variables.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theming-fallbacks-default-theme.css"> OR <link rel="stylesheet" href="{EmbeddedFiles}/theming-fallbacks-grey-theme.css">
``` 
3. Preview your applications to see the effect of changes you made

### Application Properties
The *Head* and *Theme* properties can be found by 
1. Clicking on the root node in the Application Explorer
2. Reviewing the Application properties in the properties panel

### Stadium 5
1. Add a Javascript action into the Page.load event handler
2. Paste the Javascript below into the Javascript action Code Editor popup
```
let URL = window.location.protocol + "//" + window.location.host + "/" + window.location.pathname + "//";
let el1 = document.createElement("link");
el1.setAttribute("rel","stylesheet");
el1.setAttribute("href",URL + "Content/EmbeddedFiles/theming.css");
document.querySelector("head").appendChild(el1);
let el2 = document.createElement("link");
el2.setAttribute("rel","stylesheet");
el2.setAttribute("href",URL + "Content/EmbeddedFiles/theming-variables.css");
document.querySelector("head").appendChild(el2);
let el3 = document.createElement("link");
el3.setAttribute("rel","stylesheet");
el3.setAttribute("href",URL + "Content/EmbeddedFiles/theming-fallbacks-default-theme.css");
//OR el3.setAttribute("href",URL + "Content/EmbeddedFiles/theming-fallbacks-grey-theme.css");
document.querySelector("head").appendChild(el3);
``` 

## Upgrading
To upgrade this module

1. Pull the latest repo
2. If you have made changes to the *theming-variables.css* file in your local repo, merge them
3. If new variables were added to the *theming-variables.css* file, change them as you see fit or ignore them
4. Drag the updated *theming-variables.css* file into the EmbeddedFiles folder of your application
6. Drag the *theming.css* file into the EmbeddedFiles folder of your application
7. Drag the *theming-fallbacks-default-theme.css* or *theming-fallbacks-grey-theme.css* file into the EmbeddedFiles folder of your application
8. Select "Overwrite" when prompted in Stadium

## ToDo
1. Remove !important from theme stylesheets and from kit
2. Remove & .page-content display bug when fixed