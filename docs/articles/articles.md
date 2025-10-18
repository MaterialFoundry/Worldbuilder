# Articles
<div class="imgContainer" style="max-width:50%"><img src="../../img/article/article.png"></div>


Articles are what Worldbuilder is all about.

Articles describe characters, places, items, etc. They display relevant information and images, and articles can link to other articles or Foundry documents (such as actors or scenes).<br>
This allows you to create a comprehensive database of your world.

Changes can only be made to articles when it's in [edit mode](#playedit-mode).

<div class="clear"></div>

## Basics

### Article Types
Worldbuilder has 8 different article types:

| Article Type  | Description                                                           |
|---------------|-----------------------------------------------------------------------|
| Sessions      | For session descriptions & notes                                      |
| Quests        | To describe quests                                                    |
| Characters    | To describe characters                                                |
| Groups        | To describe groups, such as guilds, organizations, etc                |
| Creatures     | To describe creatures (that don't fit in the Characters type)         |
| Locations     | To describe locations, such as countries, areas, cities or buildings  |
| Object        | To describe objects, such as important items                          |
| Other         | For anything that does not fit in the other types                     |

These article types aren't strictly enforced by Worldbuilder. They are all practically identical and the distinction is only there for convenience. The only real differences between article types are:

* Each article type has their own tab in the [main application](../mainApplication/mainApplication.md)
* Each article type has their own set of [sidebar options](#sidebar-options)

### Header Buttons
Each article has the following header buttons (at the top of the article):

| Button                                            | Action                                                                |
|---------------------------------------------------|-----------------------------------------------------------------------|
| <img src="../../img/article/playEditButton.png">  | Mode Switch: To switch between [play and edit mode](#playedit-mode)   |
| :fontawesome-solid-eye:                           | Show the article to your players, see [here](#sharing-articles)       |
| :fontawesome-solid-passport:                      | Copy UUID: Copy the UUID of the article to the clipboard              |
| :fontawesome-solid-circle-question:               | Help: Open this documentation                                         |
| :fontawesome-solid-x:                             | Close Window: Close the article                                       |

### Creating, Deleting & Duplicating Articles
You can create, delete or duplicate an article in one of the [article tabs](../mainApplication/articles.md) of the main application.

<b>Creating Articles</b><br>
Click the "+ Create New" button or use the [document import](#document-import) feature.

<b>Deleting Articles</b><br>
Right-click an article and press the ":fontawesome-solid-trash: Delete" button.

<b>Duplicating Articles</b><br>
Right-click an article and press the ":fontawesome-solid-copy: Duplicate" button.

#### Document Import
It is possible to create new articles by importing Foundry documents (actors, scenes, items, etc) into Worldbuilder. This is as simple as dragging the document from the Foundry sidebar onto the Worldbuilder application. This will open a popup to ask you the article type that the document should be imported as, click Import to create the new article.

Worldbuilder will attempt to fill in as much of the article as possible. What exactly is filled in depends on the document type, your gaming system, and your configured [sidebar options](#sidebar-options):

| Document Type | Corresponding Article Type | Filled data |
|---------------|----------------------------|-------------|
| Actor         | Characters                    | Title: Actor's name<br>Linked: Linked to actor<br>Pages\*: Biography page from character sheet<br>Images: Actor's image<br>Sidebar Options\*\*: From actor data |
| Scene         | Locations                     | Title: Scene's name<br>Linked: Linked to scene<br>Pages: From scene's linked journal entry<br>Images: Scene's background image |
| Item          | Object                        | Title: Item's name<br>Linked: Linked to item<br>Pages*: Item's description<br>Images: Item's image |
| Journal       | Other                         | Title: Journal's name<br>Linked: Linked to journal<br>Pages: Journal pages |

\* Depending on your gaming system, Worldbuilder may or may not be able to parse text from documents to generate pages. This has been tested on DnD5e and PF2E.<br>
\*\* Depending on your gaming system, Worldbuilder may or may not be able to parse select options from documents. It will attempt to match the name of a sidebar option with a key within the document's `system` object. This will only work for some sidebar options. Better support will be added in the future.

### Opening Articles
You can open an article in one of the [article tabs](../mainApplication/articles.md) of the main application, by clicking one of the articles.

### Play/Edit Mode
A worldbuilder article has 2 modes:

1. Play Mode: Articles can only be viewed
2. Edit Mode: Articles can be edited

You can switch between these modes by pressing the slider at the top-right of the article.<br>
Only players who are the [owner](#ownership) of an article can edit it.

### Sharing Articles
<div class="imgContainer"><img src="../../img/article/showArticle.png"></div>
You can share articles with other users by pressing the :fontawesome-solid-eye: icon.<br>
This will open the article for the selected users, regardless of the [ownership level](#ownership) of the user. [Secrets](#secrets) will not be shown if the user is not allowed to see them.

<div class="clear"></div>

### Creating Map Notes
<div class="imgContainer"><img src="../../img/article/mapNote.png"></div>
You can add Worldbuilder articles to the game canvas as map notes, just like Foundry journal notes. You can either drag article onto the canvas or create a new note through the Journal Notes control buttons.

Either method will open the Create Map Note dialog, where you now have a new Note Type option where you can select between journal entries and Worldbuilder articles.

!!! note "Worldbuilder Map Notes Journal Entry"
    For map notes to be clickable, they need to have a journal entry assigned to them. For this reason, when you create a Worlbuilder map note, a journal entry is created. This journal entry does not do anything useful, but should not be deleted if you want your Worldbuilder map notes to work.

<div class="clear"></div>

### Secrets
Secrets are part of an article that are only visible to users with Owner or Observer [ownership](#ownership).<br>
The following parts of an article can be made secret:

* Article pages: Will hide a page, see [here](./pages.md#secrets)
* Section of a page: Will hide part of a page, see [here](./pages.md#secrets)
* Sidebar: The entire sidebar can be hidden, see [here](#sidebar)
* Sidebar images: Will hide images in the sidebar, see [here](#images)
* Sidebar options: Will hide options, see [here](#sidebar-options)

### Ownership
<div class="imgContainer"><img src="../../img/article/ownershipConfig.png"></div>
The ownership level of an article determines what a user can or cannot do with an article.<br>
You can configure an article's ownership by right-clicking an article in the [main application](../mainApplication/mainApplication.md) and selecting "Configure Ownership".

A default ownership can be configured on the "All Players" line, or the ownership can be configured for each player individually.

The following ownership levels are available:

| Ownership level   | Article is visible| Can see secrets   | Can edit          |
|-------------------|-------------------|-------------------|-------------------|
| None              | :material-close:  | :material-close:  | :material-close:  |
| Limited           | :material-check:  | :material-close:  | :material-close:  |
| Observer          | :material-check:  | :material-check:  | :material-close:  |
| Owner             | :material-check:  | :material-check:  | :material-check:  |

## Main Section
<div class="imgContainer center">
    <img src="../../img/article/mainSection.png">
    <p class="caption">Main section of an article in play (left) and edit (right) mode.</p>
</div>

The main section of articles contain the title of the article, (optionally) linked documents, and pages of text.

### Title
You can edit the title of the article when the article is in [edit mode](#playedit-mode).

### Linked Documents
It is possible to link Foundry documents (Actors, Scenes, etc) to a Worldbuilder article. Linked documents show up at the top of the article, clicking them will open the relevant sheet of that document.

You can change which documents are linked by going into [edit mode](#playedit-mode) and dragging a document (from the Foundry sidebar) onto the box, or deleting it by clicking on the :fontawesome-solid-trash: icon of existing documents.

### Pages
The pages are the main text area of articles. See [here](./pages.md) for more information on them.

## Sidebar
<div class="imgContainer">
    <img src="../../img/article/sidebar.png">
    <p class="caption">Sidebar of an article in play (left) and edit (right) mode.</p>
</div>

The sidebar of an article contains article [images](#images), [tags](#tags) and [sidebar options](#sidebar-options).

In edit mode you can hide the sidebar or make it secret using the 2 buttons on the top-right:

| Button                    | Action                                |
|---------------------------|---------------------------------------|
| :fontawesome-solid-eye:   | Hides or unhides the sidebar          |
| :fontawesome-solid-key:   | Makes or unmakes the sidebar secret   |

### Images
You can add one or more images to an article. The first image will be used as the article's image in the [main application](../mainApplication/mainApplication.md).

When there is more than 1 image configured, buttons will appear below the image to select which image is displayed.

Clicking on an image in [play mode](#playedit-mode) will open the image in a separate window, which also has the option to show it to other players.

While in edit mode, the following buttons are available:

| Button                    | Action                            |
|---------------------------|-----------------------------------|
| :fontawesome-solid-eye:   | Hides or unhides the image        |
| :fontawesome-solid-key:   | Makes or unmakes the image secret |
| :fontawesome-solid-trash: | Deletes the image                 |
| :fontawesome-solid-plus:  | Creates a new image               |

Additionally, you can perform the following actions:

* <b>Changing Images</b>: Click on the image to open the image browser, where a new image can be selected
* <b>Renaming Images</b>: Click on the image's name to select the text editor, you can then type a new name

### Tags
You can add [tags](../tags.md) to an article. Clicking on a tag in [play mode](#playedit-mode) will open the [tag configuration](../tags.md#tag-configuration) for that tag.

See [here](../tags.md#adding-removing-tags-tofrom-an-article) for more information on how to add or remove tags from an article.

### Sidebar Options
<div class="imgContainer">
    <img src="../../img/article/sidebarOptions.png">
    <p class="caption">Sidebar options of an article in play (left) and edit (right) mode.</p>
</div>
Sidebar options are optional datafields of an article that can be useful to display important information. Depending on the [option type](./sidebarOptions.md#type), the options can display text, numbers or articles. Articles, when clicked, will open that article.

Options are only displayed in [play mode](#playedit-mode) when they have a value, are not hidden, and are not a secret (if the user is not allowed to see secrets).

The options that are available to an article depends on its [type](#article-types), and can be configured in the [options configurator](./sidebarOptions.md).

The following actions can be done when the article is in [edit mode](#playedit-mode):

<b>Changing an Option's Value</b><br>
The way you change an option's value depends on the [type](./sidebarOptions.md#type) of the option:

| Option Type   | How to Change Value                                                                                           |
|---------------|---------------------------------------------------------------------------------------------------------------|
| Textbox       | Enter in a new value.                                                                                         |
| Number        | Enter in a new value.                                                                                         |
| Select        | Select a value from the drop-down selector.                                                                   |
| Article       | Dragging an article from the [main application](../mainApplication/mainApplication.md) into the option's box. |
| Article/Text  | Adding articles: Dragging an article from the [main application](../mainApplication/mainApplication.md) into the option's box.<br>Adding text: Enter in a new value.    |

You can delete articles from options by pressing the :fontawesome-solid-trash: icon.
The Article and Article/Text options also allow Foundry documents (e.g. actors, scenes, items, etc).

<b>Hiding an Option</b><br>
You can hide or unhide an option by clicking the :fontawesome-solid-eye: icon.

<b>Making an option a secret</b><br>
You can make an option a secret by clicking the :fontawesome-solid-key: icon.