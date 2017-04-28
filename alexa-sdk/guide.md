# Updating the Alexa Skill

## Getting the code

### If installing for the first time (Cloning and installing the source code)

* In your console, navigate to where you want to install the project.

* Run `git clone git@github.com:MiamiHerald/alexa-skill.git alexa-skill` (that's the SSH url — do not use https).

* `cd` into the `alexa-skill/src/` folder and run `npm install`.

### If already installed (Pulling new code from Github)

* In your console, `cd` into the `alexa-skill` folder.

* run `git pull` to get the latest version of the site from Github.

## Editing the code

* You can use any text-editor to edit the code and the local changes will update live in your browser.

* To edit in Atom: Open new tab in console and type in `atom .` (the new tab knows you're in the alexa-skill folder).

### JavaScript

The entire Skill logic is in `src/index.js`, it includes all the prompts and card designs, session handlers and http get requests.

This file, along with the `package.json` and `node_modules`, will be compressed and uploaded to [Amazon Lambda](https://aws.amazon.com/lambda/).

### Speech Assests

In the `speechAssets` folder you will find two files: `intentSchema.json` and `SampleUtterances.txt`.

* The `intentSchema.json` defines all of the intents used to communicate with Alexa, these intents correspond with the matching intent in `src/index.js` and they are used in the Interaction Model on the [Alexa Developer Console](https://developer.amazon.com).

* The `SampleUtterances.txt` defines all speech patterns used with a given intent.  i.e. `getLatestIntent read me latest news` will invoke the `getLatestIntent` function when someone says 'Alexa, ask Miami Herald to read me latest news'.  This is also used in the Interaction Model on the [Amazon Developer Console](https://developer.amazon.com).

## Updating the source code on Github

To push your updates to Github run the following commands:

* `git add .` to stage your changes to be committed.

* `git commit -m "[your message]"` to commit your changes (add a message describing your update, so you remember).

* `git push` to push your changes to Github.

## Updating the code on Amazon Lambda and Amazon Developer console

### Amazon Lambda

* Package the following three files into a .ZIP file: `index.js`, `package.json`, `node_modules` (folder).

* Login to [Amazon Lambda](https://aws.amazon.com/lambda/) and select 'Lambda' from the list of services.

* Select the 'miamiHeraldNewsroom' function.

* Under the 'Code' tab, click 'Upload' next to 'Function Package*' and upload your new .ZIP file.

* Click 'Save'.

### Amazon Developer Console

* Login to the [Amazon Developer Console](https://developer.amazon.com) and select 'Alexa' from the top nav.

* Click 'Get Started >' under Alexa Skills Kit and select the 'Miami Herald' skill on the next page.

* Click on 'Interaction Model' and copy and paste the contents of `intentSchema.json` into the 'Intent Schema' box at the top.  Copy and paste the contents of `SampleUtterances.txt` into the 'Sample Utterances' box at the bottom.

## Help

Open an issue or e-mail chriscancodethat@gmail.com.
