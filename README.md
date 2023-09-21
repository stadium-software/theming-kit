# Stadium Theming-Kit
Prewritten CSS to create new themes for Stadium applications without writing any CSS

## Contents
The kit consists of a number of separate, but related CSS files. 
1. *theming-variables.css* contains a set of variables (this is the only file you need to make changes to!)
2. *theming.css* contains CSS to apply the variables
3. *theming-fallbacks-default-theme.css* contains the fallback variables for the Stadium default theme (Material Design Blue)
4. *theming-fallbacks-grey-theme.css* contains the fallback variables for the Grey theme

## Customisations
To customise a theme using this kit
1. Uncomment attributes to be customised in the *theming-variables.css* file
2. Amend the related values as you see fit

## Stadium 6 implementation (versions 6.6 and above)
To implement a customised theme based on the default Material Design theme
1. Drag the customised *theming-variables.css* file to the EmbeddedFiles in your application
2. Drag the *theming.css* file to the EmbeddedFiles in your application
3. Drag the *theming-fallbacks-default-theme.css* file to the EmbeddedFiles in your application
4. Create a folder called "theme" in the EmbeddedFiles in your application
5. Paste the link tags below into the *Head* property of your application
```
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming-variables.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming-fallbacks-default-theme.css">
``` 
6. Preview your applications to see the effect of changes you made

To implement a customised theme based on the Grey theme
1. Select the Grey theme in the application properties
2. Drag the customised *theming-variables.css* file to the EmbeddedFiles in your application
3. Drag the *theming.css* file to the EmbeddedFiles in your application
4. Drag the *theming-fallbacks-grey-theme.css* file to the EmbeddedFiles in your application
5. Create a folder called "theme" in the EmbeddedFiles in your application
6. Paste the link tags below into the *Head* property of your application
```
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming-variables.css">
<link rel="stylesheet" href="{EmbeddedFiles}/theme/theming-fallbacks-grey-theme.css">
``` 
7. Preview your applications to see the effect of changes you made

### Application Properties
The *Head* and *Theme* properties can be found by 
1. Clicking on the root node in the Application Explorer
2. Reviewing the Application properties in the properties panel

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