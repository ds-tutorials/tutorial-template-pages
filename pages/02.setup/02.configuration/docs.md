---
title: Configuration
taxonomy:
    category:
        - docs
---

## Site Configuration

1. Go to the **Configuration** section of the admin panel.
2. Double check that the site title is correct.
3. Double check the author name and email.
4. Edit the metadata description to describe the site.
5. Save.

## Theme Configuration

A space has been provided for the link to a git repository if using Git Sync (strongly recommended).

### Logo

1. Upload a small icon to replace the default Grav favicon.
2. Upload a logo for your organization or fill out Logo (Text) with the name of your organization.
3. Provide a URL to link to your organization's website/homepage.
4. Provide alternative text for the logo - generally this would be your institution's name. This is not necessary if using Logo (Text) instead of Logo.

!!! The file `theme.css` in `user/themes/tutorial/css/` contains an option to add an outline to an added logo link when a user hovers over it (or when it receives focus). You can uncomment this and add it to `custom.css` if you want to try it out.

### Google Analytics

This theme is set up to work with Google Analytics. If you are not planning to use Google Analytics, you can toggle this option off and ignore the rest of this section. If you are using Google Analytics, an opt out/opt back in button will be added to the footer of each page.

1. Sign in or create a [Google Analytics account](https://www.google.com/analytics/web/#home).
2. Select the **Admin** tab.
3. Select an account from the dropdown menu in the Account column.
4. Click on **Create Property** in the Property column.
5. Fill out the property settings.
6. Create a new Web Data Stream. This option will be provided immediately after creating a new property, but it can also be selected by clicking on **Data Streams** under the Property column and choosing **Add Stream**.
7. From the data stream, copy the Measurement ID (a string beginning with G-)
8. Add the measurement ID to the theme configuration (GA Measurement ID).

#### Privacy Policy

The default privacy policy reads: "This site uses Google Analytics to track anonymous usage data. We will only use this data to measure how much the tutorial is used."

If you would like to replace this text, disable the default policy and follow the instructions further down for [creating custom footer text](link-needed).

### Footer Options

#### Tutorial Maintainer

Provide the organization or other entity creating/maintaining the tutorial. You can also provide a link to the entity's website/homepage.

#### Tutorial License

Provide the license you will be sharing the tutorial under. If unsure, we recommend `Creative Commons Attribution-ShareAlike 4.0 International License`. You will also want to provide a link to the full text of the license and possibly a link to an image for the license. For example: [CC BY-SA 4.0 license](http://creativecommons.org/licenses/by-sa/4.0/), [CC BY-SA 4.0 image](https://i.creativecommons.org/l/by-sa/4.0/88x31.png).

#### Git

If using Git Sync, you may want to provide a link and the name of the hosting service (default GitHub) so viewers can access the repository.

#### Custom Footer Content

A folder called modules with a page called footer has been provided if you wish to include custom footer text. The footer page currently has no content, but any added content will be displayed in the footer on all pages. Neither the modules folder nor the footer page are routable, so they will not appear in the main navigation or the top/bottom page navigation.

If you do not have the modules folder and footer page, you can set them up manually.

1. Create a new folder and name it `modules`.
2. Under **Advanced** find "Visible" and disable it.
3. Save and return to the **Pages** tab.
4. Select **Add** (not **Add Page**).
	1. Name the new page `footer`.
	2. Set Parent Page as `/modules`.
	3. Set Visible to No.
	4. Continue and save the page.

### Other Custom Content

The theme includes files to add your own custom CSS or JavaScript if you would like to. To find these files, first go to the theme folder - `user/themes/tutorial-template`. `custom.css` is in the CSS folder, and `custom.js` is in the JavaScript folder. These files will never be modified by the theme, so you can put whatever you like in them without worrying they will be overwritten if you need to update the theme.

The file `theme.css` has a number of options you may want to copy into `custom.css` to modify. It is heavily commented to make it as easy as possible to understand what the code is doing, even if you are not familiar with CSS. Most of the options available are color choices.

## Plugin Configuration

### Git Sync

! Note: These instructions are for Git Sync version 2.1.1

#### Set up the GitHub Repository

! Note: These instructions walk through setting up Git Sync with GitHub, but you can use another hosting service if you prefer.

1. Create a new repository on GitHub.
2. Ideally the title should be the same as the directory of the Grav installation. So if you chose a directory named tableau-skyrim you would also name the git repo tableau-skyrim.
3. Include a description so you remember what the repository is for! Example: Git sync for pages in `<website name>`
4. Check the box to initialize the repository with a README file.

#### Additional Repository Setup Instructions

Since Git Sync was last updated (as of v.2.1.1), GitHub has changed the default branch for all new repositories from master to main. You will need to manually change this back to prevent issues with the plugin.

1. In your repository, click the branch dropdown with **main**.
2. Type master and then select `Create branch: master from 'main'`.
3. Go to repository Settings -> Branches.
4. Change main to master under the default branch section and click **Update**.
5. Confirm by clicking **I understand, update the default branch.**

Optional: Delete the main branch

1. Go back to the code section of the repository.
2. Click on the branch dropdown and choose: View all branches.
3. Click the trashcan to the right of the main branch.

#### Use the Git Sync Setup Wizard

1. Go to **Plugins** on the site admin panel and click on Git Sync.
2. The wizard should appear when you enter the plugin page. If it does not or if you have already dismissed it, you can click on the **Wizard** button at the bottom of the page.
3. Hosting Service
	1. GitHub
	2. Provide your GitHub username
	3. Provide your GitHub password or token. Since the wizard was created, GitHub has deprecated password use, so you will want to use a personal access token instead. Information on how to create one is included under **More Details** on the wizard.
4. Setting up the Repository
	1. You can get the HTTPS address by going to your repository, clicking the **Code** button, and copying it to your clipboard. Alternatively, you can go to your repo, copy the URL, and the add `.git` to the end.
	2. Make sure to test the connection!
5. Setting up the Webhook - follow the wizard instructions.
6. Choose What to Synchronize - stay with the default to only synchronize pages.
7. Click save

#### Finish Configuration

1. Pick your preferred settings for when to sync.
2. Refill the GitHub password/token. You will have to do this every time you make a change/save this configuration page, or else it will be incorrect.
3. Optional: Change commits author, commit message, committer name, and/or committer email.
4. Save
5. Leave page - choose to continue without saving when prompted (see note below).
6. On the left side of the admin panel, below your username, click **git** to synchronize with your repository. If everything has gone well, you will receive a notification that the sync was successful.
7. Add the link to the GitHub repository to the Tutorial Template theme configuration.

! Note: Every time you enter the Git Sync plugin configuration page, it will automatically fill out the **Git Password or Token** option with something else. If you are changing the settings at any time, make sure you have changed this back to the correct password/token before saving, or future syncs will fail. Any time you exit the page (even right after saving) you will need to continue without saving.

### Markdown Notices

1. Disable "Use built-in CSS"
2. Save