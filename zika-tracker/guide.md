# Updating the Zika Tracker

## Getting the code

### Cloning and installing the source code (Installing for the first time)

* In your console, navigate to where you want to install the project

* Run `git clone https://github.com/MiamiHerald/data-viz_zika-tracker.git zika-tracker`

* `cd` into the `zika-tracker` folder and run `npm install`.  

### Pulling new code from Github

In your console, run `git pull` to get the latest version of the site from Github.

## Starting the server

After the npm installation completes, run `npm start` to start the server (hit Ctrl+C to stop the server).

## Editing the code

You can use any text-editor to edit the code and the local changes will update live in your browser.

### HTML

The main sections of the site are split into partials located in `src/html/partials/`.  When the code is compiled for production, these partials are combined into the `index.html` file in the build folder (`public`).

### CSS

Similarly, the CSS is broken down into partials in the various folders located in `src/stylesheets/`.

### JavaScript

JS is located in `src/javascripts/modules/`.

## Updating the source code on Github

To push your updates to Github, run the following commands:

* `git add .` to stage your changes to be committed.

* `git commit -m [your message]` to commit your changes (add a message describing your update, so you remember).

* `git push` to push your changes to Github.

## Updating the code on Pubsys and Content Studio

### Uploading your files to Pubsys

* Create a production build of the project by running `npm run production`.  This will run through the production build process (minifying the CSS/JS, compiling the HTML partials, etc.), and spit out the production code to the `public` folder.

* Open your FTP client and navigate to `nm/data/MiamiHerald/MiamiHerald/static/media/projects/2016/zika-interactive-v2/`.

* Copy all the files in your local `public` folder (`index.html`, `javascripts`, `stylesheets`, etc.), to the `zika-interactive-v2` folder on Pubsys.

### Updating the `index.html` in Content Studio

* Locate the 'Daily Florida Zika virus tracker'(66790817) story in Content Studio.

* Right-click on the story and select 'Edit Source'.

* Be sure to add self closing slashes to the `img` and `source` elements. Copy the contents of `public/index.html` from `<!-- START COPY -->` through `<!-- STOP COPY -->`.

* Paste the contents in Content Studio inside `<!-- PASTE BELOW -->` through `<!-- PASTE ABOVE -->`.

* Save and Publish!

## Help

Open an issue or e-mail chriscancodethat@gmail.com.
