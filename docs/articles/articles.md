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

* <b>Sessions</b>: For session descriptions & notes.
* <b>Quests</b>: To describe quests.
* <b>Characters</b>: To describe characters.
* <b>Groups</b>: To describe groups, such as guilds, organizations, etc.
* <b>Creatures</b>: To describe creatures (that don't fit in the Characters type).
* <b>Locations</b>: To describe locations, such as countries, areas, cities or buildings.
* <b>Object</b>: To describe objects, such as important items.
* <b>Other</b>: For anything that does not fit in the other types.

<red>Expand this</red>

### Header Buttons
Each article has the following header buttons (at the top of the article):

* <img src="../../img/article/playEditButton.png"> Mode Switch: To switch between [play and edit mode](#playedit-mode)
* :fontawesome-solid-eye: Show Players: Show the article to your players, see [here](#sharing-articles)
* :fontawesome-solid-passport: Copy UUID: Copy the UUID of the article to the clipboard
* :fontawesome-solid-circle-question: Help: Open this documentation
* :fontawesome-solid-x: Close Window: Close the article

### Creating, Deleting & Duplicating Articles
You can create, delete or duplicate an article in one of the [article tabs](../mainApplication/articles.md) of the main application.

<b>Creating Articles</b><br>
Click the "+ Create New" button.

<b>Deleting Articles</b><br>
Right-click an article and press the ":fontawesome-solid-trash: Delete" button.

<b>Duplicating Articles</b><br>
Right-click an article and press the ":fontawesome-solid-copy: Duplicate" button.

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
This will open the article for the selected users, regardless of the [ownership level](#ownership) of the user. [Secrets](#secrets) will not be shown if the user is not allowed to.

<div class="clear"></div>

### Secrets
Secrets are part of an article that are only visible to users with Owner or Observer [ownership](#ownership).<br>
You can insert a secret into text sections by setting the text type to Secret (under Block), see [here](./pages.md#secrets) for more info.<br>
Data in the [sidebar](#sidebar) can also be made secret, as is explained in that section.

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
The main (big) section of articles contain the title of the article, (optionally) linked documents, and pages of text.

### Title
You can edit the title of the article when the article is in [edit mode](#playedit-mode).

### Linked Documents
It is possible to link Foundry documents (Actors, Scenes, etc) to a Worldbuilder article. Linked documents show up at the top of the article, clicking them will open the relevant sheet of that document.

You can change which documents are linked by going into [edit mode](#playedit-mode) and dragging a document (from the Foundry sidebar) onto the box, or deleting it by clicking on the :fontawesome-solid-trash: icon of existing documents.

### Pages
The pages are the main text area of articles. See [here](./pages.md) for more information on them.

## Sidebar
<red>Todo</red>

### Images
<red>Todo</red>

### Tags
<red>Todo</red>

### Options
<red>Todo</red>

#### Hiding Options
<red>Todo</red>

#### Making Options Secret
<red>Todo</red>