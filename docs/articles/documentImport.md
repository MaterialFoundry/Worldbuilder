It is possible to create new articles by importing Foundry documents (actors, scenes, items, etc) into Worldbuilder. This is as simple as dragging the document from the Foundry sidebar onto the Worldbuilder application. This will open a popup to ask you the article type that the document should be imported as, click Import to create the new article.

Worldbuilder will attempt to fill in as much of the article as possible. What exactly is filled in depends on the document type, your gaming system, and your configured [sidebar options](./sidebarOptions.md).

| Document Type | Corresponding Article Type | Filled data |
|---------------|----------------------------|-------------|
| Actor         | Characters                    | Title: Actor's name<br>Linked: Linked to actor<br>Pages: See [here](#pages)<br>Images: Actor's image<br>Sidebar Options: See [here](#sidebar-data) |
| Scene         | Locations                     | Title: Scene's name<br>Linked: Linked to scene<br>Pages: From scene's linked journal entry<br>Images: Scene's background image |
| Item          | Object                        | Title: Item's name<br>Linked: Linked to item<br>Pages: See [here](#pages)<br>Images: Item's image<br>Sidebar Options: See [here](#sidebar-data) |
| Journal       | Other                         | Title: Journal's name<br>Linked: Linked to journal<br>Pages: Journal pages |

## Gaming System Support
Worldbuilder will attempt to automatically parse system-specific data from Actors and Items.

### Sidebar Data
Actors and Items have a lot of data, such as an actor's age, eye color, height, weight, etc. Worldbuilder will attempt to extract this data from the document to automatically add this to the article's sidebar.

For this to function, it is required to configure the "System Link' in the Characters and/or Object's [sidebar options](./sidebarOptions.md).<br>
Sidebar options with a configured System Link will be populated and automatically linked.

### Pages
Based on your gaming system and the type of document, Worldbuilder will attempt to import the document's description, biography and/or GM notes. These might appear as separate pages.