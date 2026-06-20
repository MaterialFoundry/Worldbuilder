Changes between module versions are documented here.<br>

??? changelog "v1.1.1 - 20-06-2026"
    This is a minor update with some bug fixes and other changes.<br>
    Please note that while some improvements have been made with regards to detached articles and widgets, there are still some issues with them, such as when you're hovering over or clicking widget items.

    ### Additions:
    * Some fields where you can enter data (article tags, article/text sidebar options), the field will automatically be focused again, making it easy to add more data by continuing to type.
    * Added "Default Sort Mode" setting in the "User Interface" section of the settings tab.

    ### Fixes:
    * User Notes on the Home tab are now properly synchronized (saved changes are immediately visible to other players).
    * Fixed issue with the context menu not rendering (e.g. when adding a new tag to an article).
    * Widgets can now be sorted like all other articles.
    * (Foundry V14) Fixed widget panning for detached widgets and widgets in detached articles.

    ### Other:
    * Moved the "Show Players" and "Help" buttons of all applications into the core menu options (3 vertical dots).
    * (Foundry V14) Removed the "Attach/Detach" buttons for widgets, because this doesn't work properly at the moment. You can still detach widgets using Alt + Click.
    * (Foundry V14) Removed the "Change Mode" toggle for detached articles and widgets, because this doesn't work properly at the moment.

??? changelog "v1.1.0 - 13-05-2026"
    This update makes Worldbuilder compatible with Foundry v14, and it introduces a new Hierarchy widget.

    ## Highlights
    ### Foundry v14 compatibility
    Worldbuilder is now fully compatible with Foundry v14. This means that compatibility with Foundry v12 has been dropped.

    One of the new features of Foundry v14 is "detachable windows" (essentially pop-out windows), Worldbuilder is mostly compatible with it. You can detach most Worldbuilder windows, however, widgets do not work properly yet.<br>
    You can automatically detach an article by clicking it (in the main app or through one of the button inserts) while holding the alt key.

    ### New Hierarchy Widget
    This version introduces a new Hierarchy widget. This widget can be used to display, for example, family trees or organisational structures. Create items representing characters, organizations, etc, and draw lines between them to indicate how these relate to each other.<br>
    Hierarchies can be added to articles in the same way you can add map widgets and are created and edited similarly.

    ### Widget Default Item Config
    You can now configure the default config for widget items (for each widget separately). This means that, for example, you can easily change the icon color for all map items. For each config option you can choose if you want an item to use the default config or its own config.

    ### New Configuration Options for Map Widgets
    Map widgets can now be customized further with, amongst others, the addition of background image positioning, background opacity, item icon and label opacity. The legend has gotten a lot of new configuration options such as a configurable background color and opacity, border thickness and radius, configurable width, etc.

    ### Improved Data Management
    To reduce the chance of data corruption several measures have been taken, such as the introduction of a write buffer to make sure the writing of data is performed in a controlled manner. If a file cannot be read the user will now be notified with some tips on how to proceed, which should prevent accidental overwriting of data.

    ## Full Changelog
    ### Additions:
    * (Foundry v14 only) You can open articles, documents, etc detached (pop-out) by holding the alt key when opening the article. This (currently) does not work properly for widgets.
    * You can now configure whether users are allowed to create new articles (they will automatically get Owner permission), or delete owned articles. This can be configured in the Settings tab, under Permissions.
    * The widget configuration is now divided into expandable sections to make navigation easier.
    * Map widgets now have a "Default Item Config" section in the "Basics" tab, these settings will be applied to all items, unless otherwise specified.
    * Expanded the "Basics" tab of map widgets:
        * Dimensions can be configured manually
        * Added background image positioning and scaling
        * Added background color
        * Added video playback and mute settings
        * Added background opacity
    * Expanded the "Items" tab for map widgets:
        * Added icon opacity
        * Added label opacity
    * Expanded the "Legend" tab of map widgets:
        * Added configurable background color
        * Added background opacity
        * Added border thickness
        * Added border radius
        * Added width
        * Added margin
        * Added title font
        * Added title font size

    ### Fixes:
    * Dragging articles onto a `Article` or `Article/Text` sidebar option did not work, this is now fixed.
    * When panning a map widget and moving the mouse out of the widget's window, the panning would not stop when the button was released. This is now fixed.
    * Fixed issue where worldbuilder map notes pointing to non-existent articles would throw an error and prevent the scene from loading.
    * Fixed "favorites" option not showing for widgets in the main app.
    * Fixed issue where the page identifier and level were not imported if an article page was imported into a different article.
    * Changing a map widget item's type now immediately updates the item.
    * Changing the order of widget items now immediately updates which item should be on top.
    * Icon outline in the map widget is now properly hidden if the icon is set to "None".

    ### Other:
    * Improved data management: Changes are now written to a write buffer which periodically writes all buffered data. This helps prevent data corruption and reduces the amount of writes.
    * Made significant changes to how widgets are handled behind the scenes, making it much more flexible.
    * When a map widget is in edit mode, selecting an item will now automatically switch to the "Items" page in the configuration section.
    * Worldbuilder automatically creates log files which can help with debugging
    * Improved logging for debug purposes: Log files are now stored for the last 10 sessions/refreshes, and they can be easily downloaded by calling `worldbuilder.api.downloadLogs()`; 

    ### Known Issues:
    * (Foundry v14) There are some issues with widgets in detached windows related to panning, hovering, and probably other features.


??? changelog "v1.0.5 - 16-01-2026"
    This update introduces a lot of quality of life improvements, some performance improvements and some bug fixes.

    ## Highlights
    ### Article Loading Improvements
    In previous versions, when an article was opened, Foundry would load all pages of that article immediately. This could cause some performance issues on very large articles, especially when switching between edit and play mode.<br>
    In this version this has been changed. Now, only the selected page is actually loaded. This means that loading an article is much faster.

    ### Moved Page Configuration
    Instead of having all the page configuration done within the table of contents or page button, a separate section has been added right above the text editor. This keeps the table of contents and page buttons clear from all the clutter of buttons, while giving the space for additional configuration options.

    ### More Page Linking/Handling Options
    You can now drag pages or page headings from one article onto another article (in edit mode) to create a button insert to open that page/heading.
    
    Importing articles, article pages, or Foundry documents into existing articles is now possible by dragging them onto the table of contents or page buttons.

    A new "Page Identifier" option has been added to pages which allows you to replace de default page numbering (in the table of contents), and allows you to easily create map notes that visibly link to specific pages (e.g. room descriptions).

    ### Table of Contents Improvements
    The table of contents now displays which section of a page is currently visible, which can help with navigation.

    Basic page hierarchies can be made using the new `Page Level` setting, which shifts the page title slightly.

    ### Map Note Improvements
    Previously you could drop articles onto the canvas to create a map note for that article. This has been expanded with the ability to drag pages and page headings (from the table of contents) onto the canvas.

    The note configuration now has a `Headings` option to open a page on a specific heading.

    `Page Identifier` can now be used to create map notes for, for example, opening pages to room descriptions. These notes have a specific icon (circle with the page identifier as text within it), distinguishing it from normal map notes.

    ## Full Changelog
    ### Additions:
    * You can now drag article pages onto another article to create a button to open that page.
    * You can now drag headings within article pages onto another article to create a button to open that page and navigate to the heading.
    * Within an article you can now use `@WB[#heading]{title}` to create a button to navigate to a heading on the same page (lowercase, spaces must be replaced with `-`).
    * Added `Page Identifier`, which replaces the default page numbering and can be used as an identifier when dragging the page onto the canvas (see below). This is automatically imported from DnD5e `Map Location` journal pages.
    * You can now add rolls to pages. This follows the same rules as [core Foundry inline rolls](https://foundryvtt.com/article/dice/). E.g. `[[1d20]]` will create a button that displays the result of a d20 roll, `[[/r 1d20]]` will create a button to roll a d20. An addition to the core roll handling is that you can add labels, e.g. `[[/r 1d20]]{piercing damage}`. And you can reroll "immediate inline rolls" (e.g. `[[1d20]]`) by clicking on them.
    * Secrets on article pages now have a button that allows owners of that article to reveal or hide the secret. Secret background will change based on secret status (purple = secret, green = revealed).
    * Viewposition of a page is now maintained when saving a page.
    * You can now create button inserts to open compendium packs or the contents of a compendium pack.
    * Added system integration for Shadowrun 5e.
    * The TOC now displays which section of the page is currently visible.
    * Added `Page Level` which allows you to indent the page title in the TOC to create hierarchies.
    * You can now change the page order by dragging pages around in the TOC.
    * You can now drag pages, articles or documents onto the table of contents or page buttons to import them.
    * You can now drop pages or page headings (from the TOC) from an article onto the canvas to create a map note to that page and/or heading.
    * Map notes content selection has been expanded with a `Headings` option to select a specific heading on an article's page. Heading option is only visible if a page with headings has been selected.
    * Map notes content selection has been expanded with a `Use Page Identifier` option, only visible if a page has been selected. If enabled, and the page has a page identifier (see above), a circular map note will be created instead of a normal map note. This map note has the page identifier as text in the circle, and uses `Icon Tint` for the background color and `Text Color` for the text color (both as configured in the Note Config).

    ### Fixes:
    * Ownership config now has a maximum height so the "Save Changes" button is always visible, no matter how many players there are.
    * When importing a journal entry, the correct page order is now maintained.
    * Fixed issue where article thumbnails were unnecessarily deleted and recreated after each refresh.
    * Fixed TOC not correctly hiding hidden or secret pages.

    ### Other:
    * Editing a page title, icon, visibility, etc has been moved from the page button/table of contents to a separate section above the text editor.
    * The way article pages are loaded has been changed. Instead of loading all pages at once, pages are now only loaded when they are opened. This greatly improves performance when opening big articles, while (slighly) reducing performance when a new page is opened.
    * Article page buttons: Moved scrollbar down a bit to add more clearance between the scrollbar and buttons.
    * Secrets on article pages have been given a lighter background color to make them more visible.
    * When a new article is created, it automatically creates a first (empty) page.
    * Changed the default `Article Page Navigation` to `Table of Contents - Column`.
    * (Temporarily) disabled video autoplay in articles due to some (for now) unsolved issues.

??? changelog "v1.0.4 - 05-11-2025"
    ## Highlights
    This version of Worldbuilder adds compatibility with [Material Deck](https://foundryvtt.com/packages/materialdeck-premium) (Material Deck v2.1.1+ required).<br>
    Besides that, there are a number of bug fixes.

    ## Full Changelog
    ### Additions
    * Added compatibility with Material Deck

    ### Fixes
    * Checking for the existence of a backup folder and creating one when it's missing now happens earlier during initiation. So, after deleting a world's Worldbuilder data, errors regarding the backup folder not existing should no longer occur.
    * Added some checks to see if the module has finished initializing before certain actions can occur (e.g. in hooks), to prevent unnecessary errors.
    * Fixed issue where the Worldbuilder application would not load for non-GMs if no tags existed.
    * Fixed multiple issues due to sidebar options not existing after clearing data (not able to import Foundry documents, not able to create new sidebar options).
    * Link button insert will now navigate to the web, even if "https://" is note specified.
    * Video button insert now has a "video" icon instead of "image" icon.
    * Fixed issue where dragging a widget or tag onto an article would not create a button insert.

??? changelog "v1.0.3 - 26-10-2025"
    ## Highlights
    ### UI Changes/Additions
    It is now possible to change the icon, name and order of the tabs of the main application. The name and icon change will be applied throughout all of Worldbuilder (e.g. article inserts will display the new icon). The position of the tabs can also be changed so they're on the left, or the top of the application. See [here](./settings.md#tab-configuration).

    Articles have new page navigation options. Besides the buttons that were already there, you can instead choose to display a table of contents that will be automatically populated with pages and headings of the article. You can click on the pages and headings in the table of contents to navigate to the selected page/heading. See [here](./settings.md#article-page-navigation).

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
    * Table of Contents - Column: A table of contents that is displayed as a column next to the page. Clickable to open pages or navigate to a page heading
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
    * (Foundry v13 only) Linked documents now have a Worldbuilder icon in their heading where you can open the relevant articles. Not all systems might be fully supported.
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
    