---
title: Grav
taxonomy:
    category:
        - docs
intro:
    level: beginner
---

This will provide a brief overview of Grav that should be enough for working with the website. You can find additional information in the [official Grav documention](https://learn.getgrav.org/).

## The Admin Panel

The site dashboard can be accessed via the base site URL + `/admin`. You will need to log in using the username and password you provided when installing Grav.

### Updating Grav

Regularly update the website as needed. To check for updates, click the **Check for Updates** button on the top right of the admin panel dashboard.

1. If there is a new version of Grav, you can click **Update Grav Now** on the purple bar that will appear just below the updates button.
2. If themes or plugins have updates, you can click the **Update** button at the bottom right of the green Maintenance panel.
3. If there are no updates, you will see a message stating *Everything is up to date*.

### Configuration Options

At any time you can make changes to site, theme, or plugin configuration. Review the [configuration section](https://ds-tutorials.oucreate.com/grav-tutorial-demo/setup/configuration) before changing anything.

### Plugins

The **Plugins** section will provide a list of installed plugins. If needed, you can click on one of the plugins to access metadata (including a link to the ReadMe) and configuration options. You can also add new plugins by clicking the **Add** button, but this should be done with caution - make sure you understand what the plugin does and that any content it adds will be accessible to your viewers.

#### Git Sync

In addition to any automatic syncing options you have set (e.g. sync on page save), you can also sync all of your page content each time you click **git** (Synchronize GitSync) on the left side of the admin panel just below the user name). Make sure you are syncing regularly, whether automatically or manually, both so you have a backup for general purposes and so that you can restore a previous version of a page if something goes wrong.

!! Avoid going to the Git Sync plugin configuration page itself. As of version 2.1.1., every time you enter this page, it will fill out the **Git Password or Token** field with something else. If you save at any time without changing this to the correct password or personal access token first, future syncs will fail until you go back and change it. Whenever you exit the page (even right after saving) you will need to continue without saving.

#### Highlight

This provides syntax highlighting for code blocks. The tutorial template overwrites this CSS with colors that have been checked for accessible contrast levels.

### Themes

The themes page should include at least two themes - Tutorial Template and Learn2. Tutorial Template should be active. You can access the tutorial configuration options by clicking on Tutorial Template.

## Pages

### Add and Edit Pages

You can easily add pages by using the three buttons at the top of the admin panel pages section (for page, chapter, or folder). You will specify the title of the page and whether the page belongs on the top level or as the child of a folder.

The title is the first section in the editor, making it easy to change if you need to at any time (note that the title will be displayed above any content). If you do change the title, you may want to edit the folder and/or menu as described in the extra page options below.

Content is added in the Markdown editor provided, which invludes a preview button at the top right. The preview can help you check Markdown syntax, but keep in mind that the actual page will look somewhat different.

When you save your work, any changes will immediately be applied to the page in question, so you may want to keep the page open in another tab while you edit.

### Add Media

When a page is saved for the first time, a folder and document will be created for the page. After that, you can add media by clicking on the box below the content editor. Hovering over an added image will provide an option to rename it at the bottom right. If you have a lot of images, you can reorder them by dragging and dropping.

Information on including images in the page can be found in the [Markdown section](https://ds-tutorials.oucreate.com/grav-tutorial-demo/markdown).

### Extra Page Options

The page editor **Content** tab is where you will spend most of your time, but you may want to set some options in the other tabs.

#### Options

The important areas on this tab are "Published" under **Publishing** and "Category" under **Taxonomies**.

A published page with a category of `docs` will be displayed as part of the tutorial. An unpublished page will not be reachable. A published page with a category other than `docs` will be visible in the side navigation, but will not be included in the top and bottom page navigation. Thus, any pages you want to include should both be published and have the `docs` category.

#### Advanced

##### Settings

When the page is created, the name of the folder it is stored in will be the title of the page in lowercase, with spaces replaced by dashes. For example, `My Page Title` would become `my-page-title`. If the title is changed after creating the page, however, the folder name will not change automatically. This is mostly important because the folder name will be displayed as part of the page URL, so you will want to make sure that the name matches the page title sufficiently and is short and descriptive.

If the page needs to be moved to the root (top level) or to be nested inside a different folder, you can change the parent.

The page template should be Chapter, Docs, or Folder.

##### Ordering

If it is not already, you can enable folder numeric prefix here. When enabled, you can drag and drop pages to sort them. This will determine page order in the navigation, and is important. When not enabled, pages will be sorted alphabetically.

##### Overrides

The menu is how the page will be displayed in the navigation. For example, the first chapter is listed as Introduction in the menu, although its folder name is home and its title should be the same as the title of the website. If the page title is very long, it may not fit well in the side navigation or the previous page/next page navigation, so modifying the menu may be useful.

If you want to remove the page from the navigation you can disable **Routable** and/or **Visible**.

#### Chapter Options

A subtitle can be provided for any chapter. The additional metadata options - lesson level, date updated, and created by - will only be used by the first chapter, as they describe the entire lesson.

#### Expert Mode

You may notice the ability to switch between normal and expert mode. It is advisable to always stay on normal mode - expert mode should not be necessary (or helpful).