This page gives an overview of the planned features for Worldbuilder. These features are organized by category, not by priority.<br>
Although it is planned to implement these features, this is not a guarantee.

If you have an idea for a great feature, please navigate to [Feedback & Issues](./index.md#feedback-issues).

## Articles
??? changelog "User Section"
    Add a User Section (or User Pages) to articles. If a user has Limited or Observer ownership of an article, they can add their own section of text.<br>
    This could be used, for example, for users to take notes.

??? changelog "Article Templates"
    When creating a new article, provide multiple templates (based on article type) to help with the creation of the article (e.g. add Biography section for characters).

## Widgets
Widgets are objects that can be inserted into an article as an interactive element.

??? changelog "Maps: Layers"
    Add different layers to a map. For example demographic maps, boundaries.<br>
    Also item layers, so certain groups of items can be hidden or displayed (e.g. a shop layer, a landmark layer, etc).

??? changelog "Maps: Zones"
    Drawable zones. Could designate regions, neighbourhoods, etc.

??? changelog "New Widget Type: To do/checklists"
    A configurable list where list items can be added, removed or strikken through.<br>
    Can be used as a to do list, as a progress indicator, etc.<br>
    Add way to modify list entries from articles (e.g. for note taking)

??? changelog "New Widget Type: Timelines"
    Allow timelines to be inserted into an article.

??? changelog "New Widget Type: Hierarchies"
    A way to display hierarchies, such as family trees, dynasties or social rankings.

??? changelog "New Widget Type: Interactive Tables"
    For example:<br>
    Pricelists for shops<br>
    (Rollable) loot tables

## Automation & Gaming Systems

??? changelog "Improved Gaming System Integrations"
    Parse article data from actors.<br>
    Add (rollable) insertables, such as HP bars, skills, abilities, etc.

## Data Management

??? changelog "Allow Data Sharing & Edits Through Sockets"
    Currently, non-GM players need the "Upload New Files" permission in order for them to edit articles, and users of the Forge require addition setup to even see articles.
    Allowing data sharing through sockets allows articles to be opened and edited without any special permissions, but the GM needs to be online.

??? changelog "Import & Export Single Articles"
    Allow single articles to be exported or imported.

??? changelog "External Backups"
    Allowing backups to be saved somewhere else (Google Drive, Dropbox, etc).

??? changelog "Content Creator Import Method"
    A conventient way for contenct creators to bundle Worldbuilder articles with their content.<br>
    For example, actors could bundle a character article, scenes could bundle a location article, etc.<br>
    Ideally, entire campaigns could be imported.

??? changelog "Selective Article Sharing Between Different Worlds"
    Right now it is possible to share all Worldbuilder data between different worlds on the same server (see [here](./dataManagement.md#data-id)).<br>
    This feature will add a way to configure this on an article-by-article basis. So if you run multiple games with the same campaign, you could share all NPC characters, locations, etc between the different worlds, while keeping PC characters and other articles relevant to specific games separate.

## Other

??? changelog "Calendar System"
    Either use another module (such as [Simple Calendar](https://foundryvtt.com/packages/foundryvtt-simple-calendar)), or create a new calendar system.<br>
    Integrate this calendar into the Timelines feature, link it to relevant article data (such as birth dates), insert dates or (partial) calendars into articles, etc.

??? changelog "Themes"
    Change how Worldbuilder appears. Configure backgrounds and colors.