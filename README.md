# Enviroment
Install Nodejs modules and Gulp tools.
    `npm install`
    `guld sass`
    `guld localhost`


# I. New Page To top 
To create a new page, you can use layout_blank_page.html which provides basic page layout which you can extend and modify further.

# II. GULP Tasks To top 
Gulp is a toolkit that will help you automate painful or time-consuming tasks in your development workflow. To get started first install Node.js as gulp require npm to run. It can be downloaded at http://nodejs.org/download/. We can now install Gulp using npm. To install Gulp just follow below steps:

Launch cmd.exe or any relevant command line tool and change the directory into the theme's root, where the gulpfile.js is located.
Run npm install to install the required gulp dependencies.
Run npm install gulp -g to ensure Gulp is available globally for any project.


1. Local Server

Launch cmd.exe or any relevant command line tool and CD to your theme directly where gulpfile.js is located.
Run gulp localhost command to start the localhost server. Now you can open up localhost:7080 in our browser, where you will see list separate theme demo folders
NOTICE: Some ajax datatable demos will not be available when gulp localhost task is used. To fully run the theme with ajax data source demos please deploy the theme into a local server with Apache and PHP support.
For more info you can visit the plugin's official documentation here.


2. SASS Compilation

Launch cmd.exe or any relevant command line tool and CD to your theme directly where gulpfile.js is located.
Run gulp sass command to run the build task manually.
Run gulp sass:watch to run the scss file watcher task to compile the css files realtime.
The compiled css files will be generated in the assets. 

3. RTL SASS Compilation

Launch cmd.exe or any relevant command line tool and CD to your RTL theme folder(theme_rtl) directly where gulpfile.js is located.
Make sure the recently modified SCSS files are compiled with gulp sass or gulp sass:watch task.
Run gulp rtlcss command to run the task to monify the RTL version of the css files.
The compiled RTL css files will be generated in the assets directory. 

4. CSS & JS File Minification

Launch cmd.exe and CD to your theme directly where gulpfile.js is located
Run gulp minify command to run the task to minify the theme's css and js files.
The minified files will be generated the assets directory.

# III. Coding & Extending To top 
# CSS
To overide the theme CSS styles you can use ../assets/layouts/layout/css/custom.css for your own customization. This will make the future updates easier if you keep your own CSS code seperate.

# Excluding Unused Resources
Assumes you selected Admin 1(admin_1) sub theme from available 7 sub themes.
There are 2 main parts of the theme. First is the assets folder that contains all the css, js and 3rd party plugins and the templates folder where actually HTML templates are placed. So refer to theme/assets and theme/admin_1 folders to get started.

In theme/assets folder you can see separate folder for layouts(admin 1, admin 2, .... admin 7) and you can keep the assets of the layout you are using(theme/assets/layouts/layout) and also the global assets(theme/layouts/global) and the rest layout assets you can remove since your selected layout does not use them. So under theme/assets/layouts folder you will have theme/assets/layouts/layout and theme/assets/layouts/global folder only.

From theme/admin_1 refer to the started layout_blank_page.html template. This template includes the minimal required css, js and 3rd party plugins. You can use this template as starting point to your application pages.
Try to separate the HTML code of layout_blank_page.html into modular partials(header, sidebar, footer, main content) and keep the partials centralized for each page.

Under 3rd party plugins folder(theme/assets/global/plugins) you can exclude unused plugins if you need. By default metronic includes over 80 3rd party plugins and most of theme you may not use so you can exclude the ones you will not use.

#IV. Javascript Plugins & Resources