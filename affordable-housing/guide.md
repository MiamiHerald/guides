# Updating the Affordable Housing Tool

## Getting the code

### If installing for the first time (Cloning and installing the source code)

* In your console, navigate to where you want to install the project.

* Run `git clone git@github.com:MiamiHerald/data-viz_miami-dade-housing-costs.git affordable-housing-tool` (that's the SSH url — do not use https).

* `cd` into the `affordable-housing-tool` folder and run `npm install`.

### If already installed (Pulling new code from Github)

* In your console, `cd` into the `affordable-housing-tool` folder.

* run `git pull` to get the latest version of the site from Github.

## Starting the server

After the npm installation completes, run `gulp` to start the server (hit Ctrl+C to stop the server).

## Editing the code

* You can use any text-editor to edit the code and the local changes will update live in your browser.

* To edit in Atom: Open new tab in console and type in `atom .` (the new tab knows you're in the zika-tracker folder).

### HTML

The majority of the HTML is located in `app/templates/index.html`.  There is the `app/templates/base.html` partial and `app/templates/includes` partials, but these are only required for local development and are not required for production.

When the code is compiled for production, the `app/templates/index.html` is copied into the `build/app/` folder.

### CSS

The CSS is broken down into partials in the various folders located in `app/scss/`.

### JavaScript

JS is located in `app/js/`.  The majority of the JS is in `main.js` and `functions.js`.

## Updating the source code on Github

To push your updates to Github, stop the server (using ctrl-C) and run the following commands:

* `git add .` to stage your changes to be committed.

* `git commit -m "[your message]"` to commit your changes (add a message describing your update, so you remember).

* `git push` to push your changes to Github.

## Updating the code on Pubsys and Content Studio

### Uploading your files to Pubsys

* Create a production build of the project by running `gulp build`.  This will run through the production build process (compiling the CSS, copying the HTML/JS/CSS, etc.), and spit out the production code to the `build/app/` folder.

* Open the local folder (hint: you can run `open .` to launch it in your browser).

* Open your FTP client and navigate to `nm/data/MiamiHerald/MiamiHerald/static/media/projects/2016/housing-prices-update/`.

* Copy all the files in your local `build/app/` folder (`index.html`, `js`, `css` and `img`), to the `housing-prices-update` folder on Pubsys.

### Updating the `index.html` in Content Studio

* Locate the 'See where you can afford a home in South Florida'(120650903) story in Content Studio.

* Right-click on the story body and select 'Edit Source'.

* Copy the contents of `public/index.html` from `<!-- START COPY -->` through `<!-- STOP COPY -->`.

* Paste the contents in Content Studio starting with `<div ng-app="housingApp">` through the last `</div>` element.

* Save and Publish!

## Help

Open an issue or e-mail chriscancodethat@gmail.com.
