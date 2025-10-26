Changes between module versions are documented here.<br>

??? changelog "v1.0.3 - 26-10-2025"
    ## Highlights
    ### UI Changes/Additions
    It is now possible to change the icon, name and order of the tabs of the main application. The name and icon change will be applied throughout all of Worldbuilder (e.g. article inserts will display the new icon). The position of the tabs can also be changed so they're on the left, or the top of the application. See [here](./settings.md#tab-configuration).

    Articles have new page navigation options. Besides the buttons that were already there, you can instead choose to display a table of contents that will be automatically populated with pages and headers of the article. You can click on the pages and headers in the table of contents to navigate to the selected page/header. See [here](./settings.md#article-page-navigation).

    ### Improved Gaming System Integration
    Sidebar options can now be configured to automatically parse specific data from Actor and Item documents (e.g. an actor's age, item's weight, etc). This can be configured that changes in the document are automatically updated in the article, and vice versa. See [here](./articles/articles.md#system-link) for more information on how to configure this. Worldbuilder will also do a better job at converting biographies, descriptions and GM notes into pages. 

    The amount of support depends on your gaming system. Support has been specifically added for the following systems, but others will probably also work (partially): DnD5e, PF1, PF2e, SWADE, WFRP4E, Starfinder, DC20, Forbidden Lands, Call of Cthulhu 7, Simple Worldbuilding.

    ### Improved Drag & Drop
    Article and document button inserts can now be dragged onto other articles or documents. You can also drag articles onto, for example, journal entries, to create a button that will open the article.

    Dragging actors from an article onto the canvas will create a token, dragging other documents or articles onto the canvas will create a map note that opens that document/article.

    ### Searching for Articles Using their Content
    You can now search for articles based on the content of their pages using `content:"search term"`.<br>
    For example, if you want to find articles that contain the text "the old tavern" on one of their pages, you can search using `content:"the old tavern."`.

    ## Full Changelog
    ### Additions
    #### UI
    * You can now change the icon, name and order of the tabs of the main application.
    * The tabs of the main application can now be moved to the top or left.
    * Added configurable article page navigation. You can now choose between:
    * Buttons: Buttons at the top that open a page when clicked (as it was previously)
    * Table of Contents - Column: A table of contents that is displayed as a column next to the page. Clickable to open pages or navigate to a page header
    * Table of Contents - Sidebar: Similar to the Column option, but the table of contents is displayed as a sidebar on the left of the article

    #### Gaming System Integration
    Support has been added for the following systems, but other system are probably partially supported as well: DnD5e, PF1, PF2e, SWADE, WFRP4E, Starfinder, DC20, Forbidden Lands, Call of Cthulhu 7, Simple Worldbuilding.

    * The way data can be gotten from Actor and Item documents has been improved. Worldbuilder will attempt to find out which data from these documents can be relevant to be displayed in the article sidebar. Things like Alignment, Age, Race, Class, etc. When importing a document into Worldbuilder, the relevant sidebar fields will be automatically populated and linked to the document. This means that, if configured, changes in an actor can be reflected in a linked article (e.g. if "Hair Color" is changed to "Brown" in the document, the article to also display "Brown").
    * The Characters and Objects "Sidebar Options Configurator" has a new System Link option, to allow you to configure which document data will be used for that sidebar option.
    * In the sidebar of articles that have a document linked, options that have a System Link configured will display an icon to either link that option to the document, or to use a custom input.
    * When importing actors and items, automatic creation of articles pages has been improved (biography page, gm notes page, etc).

    #### Drag & Drop
    * You can now drag & drop article/document buttons from one article onto another article or onto a document (such as journal entries, character sheets, etc).
    * Dragging article/document buttons from an article onto the canvas will create a token or map note.
    * When importing a document, the ownership of that document is also applied to the article.
    * (Foundry v13 only) Linked documents now have a Worldbuilder icon in their header where you can open the relevant articles. Not all systems might be fully supported.
    * You can now search articles by their content: `content:"search term"`

    ### Fixes
    * Fixed the article button insert configuration for Foundry v13
    * Changing the "Click" for map items would throw an error, preventing changes from being saved, this is now fixed
    * Fixed issue where it sometimes wasn't possible to add a second value to an "Article/Text" sidebar option
    * Tags App: 
    * Parent & sub-tag context menu no longer shows up when in play mode
    * Parent & sub-tag context menu no longer displays the selected tag
    * Tags can no longer be made their own parent or sub-tag
    * Fixed sub-tag name (was Sub-Tabs)

    ### Other Changes
    * In the Options Configurator, the "Textbox" type has been renamed to "Text"
    * Article sidebar option visibility has been improved in light mode when in Play mode
    * Removed text shadow in Options Configurator and Backup Manager headers to improve readability in light mode
    * When an article is in edit mode, the hints for "Title" and "Linked" have been replaced by tooltips
    * Replace the "Edit Sidebar Options" button in the article sidebar with a small icon
    * Moved the "Display Tab Titles" setting to the new "User Interface" category
    * Merged "tabVisibility" setting into the "tabConfig" setting
    * Merged "displayTabTibles" setting into the "ui" setting
    * Changed the article scroll behavior: Title and linked documents will stay visible, scrolling happens below that.

??? changelog "v1.0.2 - 18-10-2025"
    ## Highlights
    ### More ways to open Worldbuilder
    * A control button (on the left side of the screen) has been added to open Worldbuilder.
    * A configurable hotkey has been added to open Worldbuilder (`Alt+W` by default).

    ### More control over what players can see
    * It was already possible to make parts of articles secret or hide them, but this version expands on that. It is now possible to make article pages and images secret, or hide them from everyone. Similarly, you can now hide the entire sidebar, or make it a secret.
    * You have now greater control over which tabs in the Worldbuilder application are visible. Previously you could either show or hide them for everyone, but you can now hide them only for players, or hide them for players if they do not have at least 1 relevant article that they have Limited or higher ownership over.

    ### Data sharing between worlds
    * It is now possible for different worlds on the same Foundry server to use the same Worldbuilder data. If, for example, you run multiple "Curse of Strahd" games, you can have them share the same data so you don't have to recreate the same articles for each world. More info [here](https://materialfoundry.github.io/Worldbuilder/dataManagement/#data-id).

    ## Full Changelog
    ### Additions
    * You can now open Worldbuilder articles through map notes. Dropping articles on a scene will automatically create a map note.
    * You can now drag Foundry documents (actors, items, etc) onto a "Article" or "Article/Text" sidebar option.
    * Added hotkeys to open/close the Worldbuilder application (Alt+W) and to close all Worldbuilder windows (Alt+A), can be configured in Foundry's Controls Configuration.
    * Added a control button to open Worldbuilder.
    * Added new tab visibility modes for the main application: Besides showing and hiding tabs, you can make them GM-only, or hide them when a player has no relevant articles that they can see.
    * Added a new Data Id setting, which allows you to share your Worldbuilder data between different worlds on the same server.
    * Article pages and images can now be made secret or hidden.
    * The entire article sidebar can be made secret or hidden.

    ### Fixes
    * Fixed UI bug for the main app tabs when using Carolingian UI.
    * Fixed issue with user notes not saving.
    * Fixed an issue when trying to clear data in v12 that would prevent Worldbuilder from loading.
    * Clear Data button now works in v13.
    * Fixed issue where linked documents in articles could not be deleted.
    * If there were too many article pages or images that the page/image buttons would be wider than the enclosing element, the left-most button(s) would be (parially) unreachable. This is now fixed.
    * Forbidden Lands: The article images section would not be displayed if there were no images configured. This is now fixed.
    * Asset folder on Sqyre servers should now be accessible through the Worldbuilder file picker.

    ### Other Changes
    * Changed Worldbuilder icon (in Settings sidebar) to a globe.

??? changelog "v1.0.1 - 18-10-2025"
    Something went wrong with this release, so it was removed.

??? changelog "v1.0.0 - 15-10-2025"
    Initial release.
    