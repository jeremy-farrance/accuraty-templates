# Accuraty templates

This is a set of standards, common components, and best practices for projects in a way that is easy to deploy using modern web technologies and up-to-date frameworks. Accuraty primarily works with the DNN content management system. The files included are a starting point for this platform.

## Project requirements

- DNN site already deployed
- [Node v10.15.2](https://nodejs.org/en)

## Getting started

### Initial setup

_This assumes the project skin has not been set up at all. If the project already exists on GitHub and you are trying to get set up on your own machine, skip to [Ongoing development](https://github.com/chrismlusk/accuraty-templates#ongoing-development)._

#### 1. Get the code

Create a new project folder on your local machine, `cd` into that directory, and run the following commands in your terminal:

```
git init
git remote add accuraty https://github.com/chrismlusk/accuraty-templates.git
git fetch accuraty
git merge accuraty/master
```

#### 2. Set your FTP config

If you are using Visual Studio Code, navigate to the `.vscode/` directory. Copy `sftp.json.example`, configure it with your credentials, and save it as `sftp.json`.

#### 3. Set the project name

Next, navigate to the Skin folder:

```
cd Portals/_default/Skins/CLIENT_CODE
```

Then, open `package.json` and change the `name` property from "CLIENT_CODE" to whatever the project's name should be. This name will be used in multiple places (e.g., the Skin and Container directories, as a Sass variable, the EasyDNNnews template name), but **you only need to set it here**. The Gulp build process takes care of setting the name everywhere else.

_Note: Although the placeholder name is in all caps, NPM rules require the name to be lowercase._

#### 4. Install packages

Run `npm install` from inside the Skin folder.

#### 5. Build the assets

Then run `npm start` in your terminal.

This will kick off the Gulp tasks to initialize the project, compile starting assets, and begin watching for changes to source files.

To exit this "watch" mode, press `Control-C` in your terminal.

To start watching again, run `npm run dev` in your terminal.

### Ongoing development

_This assumes the project has already been set up and added as a repository to the [Accuraty GitHub account](https://github.com/Accuraty)._

#### 1. Get the code

Navigate to the directory where you want to store the project, copy the GitHub URL, and then run the following commands in your terminal:

```
git clone [PASTE_THE_GITHUB_URL_HERE]
```

#### 2. Set your FTP config

If you are using Visual Studio Code, navigate to the `.vscode/` directory. Copy `sftp.json.example`, configure it with your credentials, and save it as `sftp.json` to continue.

#### 3. Install packages

Next, `cd` into the skin (`Portals/_default/Skins/[ABBV]`) and run `npm install` to get the required packages.

#### 4. Build the assets

Then run `npm start` in your terminal.

This will kick off the Gulp tasks to initialize the project, compile starting assets, and begin watching for changes to source files.

To exit this "watch" mode, press `Control-C` in your terminal.

To start watching again, run `npm run dev` in your terminal.

## About Accuraty

**Accuraty Solutions** is a full-service website firm that provides a wide range of web services: design, development, applications, hosting, e-commerce, and more. We deliver creative, effective results and have extensive experience in building useful online presences for businesses, organizations, and communities.

---

Reference: [Accuraty Solutions](http://www.accuraty.com)
