# Stadium Theming-Kit
A set of CSS variables for making adjustments to the default theme of Stadium applications

## Description
This kit consists of three separate, but related CSS files

1. *theming-variables.css* contains a set of variables
2. *theming.css* contains a number of CSS instructions
3. *theming-fallbacks-default-theme.css* contains the fallback variables for the Material Design (Stadium default) theme

## How-to (simple)
To customise the default theme

1. Uncomment attributes to be customised in the *theming-variables.css* file
2. Amend the related values as you see fit
3. Copy and paste the contents of both files into the StyleSheet editor of your application
4. Preview the application to see the applied styles

## How-to (advanced)
If you have a webserver installed on your machine, you can use this more efficient development setup 

1. Place the CSS files into a folder under the webserver 
2. Add a link to each stylesheet into the "Head" property of your application, pointing to the stylesheets as below
```
<link rel="stylesheet" href="http://localhost:8888/theming-kit/theming.css">
<link rel="stylesheet" href="http://localhost:8888/theming-kit/theming-variables.css">
```
3. Preview your Stadium application
4. Open the theming-variables.css file in your favourite editor (I recommend VSCode)
5. Edit the CSS variables as you see fit
6. Hit "Refresh" in the browser to see the styles applied to your application

If you use this method, you can copy the styles into your application as per the simple method above when you go live. 

## Getting a local webserver
You can go into your *Control Panel* -> *Programs and Features* -> *Turn Windows Features on or off* and switch on *Internet Information Services* to install IIS on your Windows machine. 

If you have Python 3 installed, you can try this: https://stackoverflow.com/questions/5050851/best-lightweight-web-server-only-static-content-for-windows

Other webservers can be found here: https://www.elegantthemes.com/blog/wordpress/best-web-servers-for-windows-and-linux

More webservers are only Google a search away...