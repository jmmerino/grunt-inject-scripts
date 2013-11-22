grunt-inject-scripts

#Author

Jesús Merino, based on Pedro Rocha "grunt-script-inject"

# Description

Automatically injects script tags into a page. Nice for auto put script tags in angular apps.

#   Example (gruntfile.js):

    scriptinject: {
        dev: {
            srcs: ['src/frontend/modules/app.js', 'src/frontend/modules/*/*.js', 'src/frontend/modules/*/*/*.js'], //order is important if this sciprt will be concated and minified
            html: 'src/application.html', //file that as the block comment to look for a place to insert the script tags
            without: 'src/', //this script will be used to remove this block of string of script tag file location
            template: '<script>%file_path%</script>' //Used to modify the template that is going to be injected. The string "%file_path%" will be replaced with the path of the file injected.
        }
    }


# Example of HTML if block:

    <!-- scriptinject begin -->
    //everything here will be replace by all script loaded. You can run this task many times you want.
    <!-- scriptinject end -->
