---
title: Installation
taxonomy:
    category:
        - docs
visible: true
intro:
    level: beginner
---

These are instructions for installing Grav using OU Create (or Reclaim Hosting). If you are using a different hosting service, you may want to check out the [Grav installation documentation](https://learn.getgrav.org/basics/installation).

## Install Grav on OU Create

If you would like to use OU Create but have not yet set up an accout, visit the [OU Create documentation](https://create.ou.edu/docs/getting-started/general-information/) to get started.

On your OU Create dashboard, select Grav from the Applications section and click **install this application**. Installation settings you will want to change are specified below. Everything else can be left as-is.

### Location

1. Choose the domain where the tutorial will be installed. You will want to pick an option that includes "https" but does not include "www." For example: `https://ds-tutorials.oucreate.com`.
2. Choose a simple name for the directory that will differentiate this tutorial from any others you create. Good practice is for the directory to be all lowercase with words separated by dashes. For example: `tableau-skyrim`.

### Settings

1. You will want a longer/more descriptive site title. For example, `tableau-skyrim` might become `Visualizing Data with Tableau`.
2. Full name should most likely be your name or the name of your institution. For example: `Digital Scholarship @ OU Libraries`.
3. Choose the email address you would like associated with the tutorial installation.
4. Make sure to pick the username and administrator password. OU Create will automatically generate a random password, so if you want to use that, make sure you know what it is first.
5. The skeleton package should be: Grav Core + Admin (Default)

### Finishing

Once you have modified the settings, go ahead and click Install.

You can then access your website directly via its address, or by going to the OU Create dashboard, clicking on My Apps under the Applications section, and finding the tutorial in the list of installed applications.

The admin panel can be accessed by clicking the 2nd link provided on the OU Create My Apps page, or by appending `/admin` to the website URL.

## Non-OU Create Installs

If you are using a different hosting service, make sure you have checked out the [Grav installation documentation](https://learn.getgrav.org/basics/installation).

If your installation does not automatically come with the following plugins, you will want to add them:
- Admin Panel
- Email
- Error
- Flex Objects
- Form
- Login
- Markdown Notices
- Problems

These are all official Grav plugins.

## Basic Setup

For these instructions, you will need to go to the admin panel for your site (Website URL + `/admin`).

### Check for Updates

The first thing to do, once you get to the site dashboard, is update Grav. You will want to do this periodically as part of your tutorial upkeep.

1. Click the **Check for Updates** button on the top right.
2. If there is a new version of Grav, a purple bar will appear at the top of the page with an **Update Grav Now** button. Click this button and wait for the update to finish before proceeding.
3. If any of your plugins or themes have updates, there will be an **Update** button available at the bottom right of the green Maintenance panel. Click this and click Continue if/when prompted. You may receive a notification that certain dependencies are required - clicking Next or Continue will install them automatically for you.
4. You can click **Check for Updates** again to doublecheck that everything is 100% up to date.

### Add Themes

1. Select **Themes** from the admin panel navigation.
2. Choose **Add** (button at the top right).
3. Look for the theme Tutorial and click **Install**.
4. You should receive a notification that the theme requires learn2 as a dependency. This is because Tutorial inherits from the Learn2 theme and requires it to work. Click **Continue** and Grav will install both themes.
! Note: As of February 10, 2021, Learn2 has an issue where it may not show up in you Admin Panel themes. Do not worry if that is the case: As long as Learn2 has been installed, Tutorial should work.
5. Do not bother with any of the configuration settings yet. Click **Back to Themes**.
6. Activate the Tutorial theme.
7. Optional: Uninstall the Quark theme. (Click on the theme to see configuration options and an uninstall button).

### Add Plugins

Go to **Plugins** on the admin panel and click **Add** to add each of the following plugins:

- Admin Addon Media Rename
	- This will allow you to rename any media files you upload directly from the admin panel.
- Custom CSS
	- This will allow you to modify the website styles without having your changes overwritten by updates.
- Git Sync
	- This will allow you to sync your pages with a git repository.
	- **Note:** The configuration wizard will pop up once this is installed. You can cancel for now or jump ahead to the [plugin configuration](https://ds-tutorials.oucreate.com/grav-tutorial-demo/setup/configuration#plugin-configuration). When navigating away from the page, click **Continue** at the unsaved changes prompt.
- Highlight
	- This provides syntax highlighting for any code sections you include.
- Shortcode Core
	- This provides several useful Markdown shortcodes that add to what you can include in your tutorial.