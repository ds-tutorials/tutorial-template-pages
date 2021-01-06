---
title: 'Tutorial Structure'
taxonomy:
    category:
        - docs
intro:
    level: beginner
---

! Note: This is a recommended structure that will make the most of the provided theme.

## First Chapter

The first chapter requires special configuration that is provided for you, so be sure not to delete the sample page. Instead, edit the page and replace the current title and content as follows:

1. The title of the first chapter should be the same as the title of the tutorial/website.
2. In **Chapter Options**, the subtitle should provide a brief description of the tutorial.
3. In **Chapter Options**, the three pieces of metadata should be set (and updated later as needed) - lesson level, last updated, and created by.
4. You will probably want to include the following in the page contents:
	1. A brief explanation of the tutorial contents and if possible an example of the finished product
	2. Any prior knowledge or experience required
	3. Any useful reference materials
	4. Setup instructions for downloading data, installing software, etc.

If the first page is missing for any reason, you can manually edit the page header by switching from Normal to Expert mode in the admin panel page editor and add the line `isIntro: true`.

## Folder Structure

You can nest chapters and pages inside folders if the tutorial requires additional structure. These pages demonstrate one level of nesting, but you can do more if you want. Be aware that a page should never serve as a folder/container for another page. Such a page will become inaccessible from the main navigation and may cause issues with the previous/next page navigation.

The admin panel includes an **Add Folder** button in the Pages section that will automatically create a folder that is visible but not routable. In general, even if you do not use this button, as long as folders are visible but not routable they should function as needed.

## Chapters and Pages

The contents of the tutorial will exist in normal pages (docs) or chapters. Chapters mark the beginning of a new section of content and will typically be the first page within a top level folder.

- Chapters will have the option to include a subtitle.
- The additional metadata (lesson level etc.) in **Chapter Options** will be ignored by all but the first chapter.
- All pages to include in the tutorial must have **Category** set to `docs`. This should happen automatically when creating a new docs or chapter page.