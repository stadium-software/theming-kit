# Stadium Theming-Kit
Prewritten CSS to create new themes for Stadium applications without writing any CSS

https://github.com/stadium-software/theming-kit/assets/2085324/6762e574-d2c7-4604-a8df-6adf837f5214

## Description
This kit currently supports adjusting applications based on the Default or the Grey themes. To find out which theme an application uses, see [Application Properties](#application-properties) below

## Sample applications
This repo contains two Stadium 6.7 applications
1. [Theming_Kit_Default.sapz](Stadium6/Theming_Kit_Default.sapz?raw=true)
2. [Theming_Kit_Grey.sapz](Stadium6/Theming_Kit_Grey.sapz?raw=true)

## Version
1.1 - fixed some bugs (thanks Ethan!)

## Contents
The kit consists of a number of separate, but related CSS files
1. *theming-variables.css* contains a set of variables (this is the only file you need to make changes to!)
2. *theming.css* contains CSS to apply the variables
3. *theming-fallbacks-default-theme.css* contains the fallback variables for the Stadium default theme (Material Design Blue)
4. *theming-fallbacks-grey-theme.css* contains the fallback variables for the Grey theme
5. Two sample applications you can use to develop a theme. These applications require the [Samples Database](https://github.com/stadium-software/samples-database)

## Customisations
To customise a theme using this kit
1. Uncomment attributes to be customised in the *theming-variables.css* file
2. Amend the related values as you see fit
3. Control-specific values override general form values

## Stadium 6 implementation (versions 6.6 and above)

### Default Theme
1. Make sure the Default theme is selected in the [application properties](#Application-Properties)
2. Drag the customised *theming-variables.css* file to the *EmbeddedFiles* in your application
3. Drag the *theming.css* file to the *EmbeddedFiles* in your application
4. Drag the *theming-fallbacks-default-theme.css* file to the *EmbeddedFiles* in your application
5. Create a folder called "Theme" in the *EmbeddedFiles* in your application
6. Paste the link tags below into the *Head* property of your [application properties](#Application-Properties)
```html
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming.css">
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming-variables.css">
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming-fallbacks-default-theme.css">
``` 
1. Preview your applications to see the effect of changes you made

### Grey Theme
1. Make sure the Grey theme is selected in the [application properties](#Application-Properties)
2. Drag the customised *theming-variables.css* file to the *EmbeddedFiles* in your application
3. Drag the *theming.css* file to the *EmbeddedFiles* in your application
4. Drag the *theming-fallbacks-grey-theme.css* file to the *EmbeddedFiles* in your application
5. Create a folder called "Theme" in the *EmbeddedFiles* in your application
6. Paste the link tags below into the *Head* property of your [application properties](#Application-Properties)
```html
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming.css">
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming-variables.css">
<link rel="stylesheet" href="{EmbeddedFiles}/Theme/theming-fallbacks-grey-theme.css">
``` 
7. Preview your applications to see the effect of changes you made

## Application Properties
To locate the *Head* and *Theme* properties
1. Click on the root node in the Application Explorer
2. Review the Application properties in the properties panel

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
