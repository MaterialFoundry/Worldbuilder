Worldbuilder provides multiple search bars where you can search for articles or tags.<br>
Most tabs of the [main application](./mainApplication.md) have a search bar at the top. This search bar allows for searches of that article type or tag.

## Searching by Name
The default search functionality is to search by name. If you enter a search term into the search bar it will filter the articles so only articles that contain that term will be displayed.<br>
Each separate word is a separate search term, so you will get results if any of the words match. You can force multi-word search terms using quotation marks `"`.<br>
Search terms are case-insensitive.

<b>Examples:</b><br>
Searching `t` will result in all articles that have "t" in their name.<br>
Searching `tavern` will result in all articles that have "tavern" in their name.<br>
Searching `the old tavern` will result in articles that have "the", "old" or "tavern" in their name.<br>
Searching `"the old tavern"` will result in articles that have "the old tavern" in their name.

## Searching by Tag
You can search for articles that have a certain tag.<br>
The search terms will take the form `tag:(tag)`, where `(tag)` is the name of the tag.<br>
You can search for multiple tags at the same time using `tag:[(tag1) (tag2)]`. This is essentially the same as `tag:(tag1) tag:(tag2)`.<br>
The tag name search term is similar to [searching by name](#searching-by-name), except that they have to match exactly (but still case-insensitive).

<b>Examples:</b><br>
Searching `tag:house` will result in all articles that have the "house" tag.<br>
Searching `tag:"house lenora"` will result in articles that have the "house lenora" tag.<br>
Searching `tag:[house "house lenora"]` will result in articles that have the "house" or "house lenora" tag.

<b>Wrong examples:</b><br>
Searching `tag:hou` will <u>not</u> result in articles that have the "house" tag, but articles that have the "hou" tag.<br>
Searching `tag:house lenora` will <u>not</u> result in articles that have the "house lenora" tag, but articles that either have the "house" tag or have "lenora" in their name.<br>

## Searching by Content
You can search for articles based on their content (what's written in their pages).<br>
This is very similar to [searching by tag](#searching-by-tag), except that you replace `tag:` with `content:`.

<b>Examples:</b><br>
Searching `content:tavern` will result in all articles that have the word "tavern" on one of their pages.<br>
Searching `content:"the old tavern"` will result in all articles that have the words "the old tavern" (in this exact order) on one of their pages.

<b>Wrong examples:</b><br>
Searching `content:old tavern` will <u>not</u> result in articles that have the words "the old tavern" on one of their pages. Instead it will return articles that have the word "old" on one of their pages <u>and</u> articles that have "tavern" in their name.

## Searching by Sidebar Option
[Sidebar options](../articles/sidebarOptions.md) are the configurable settings in the [sidebar](../articles/articles.md#sidebar) of articles.<br>
You can search for articles that have a specific sidebar option.<br>
This is very similar to [searching by tag](#searching-by-tag), except that you replace `tag:` with `(option):`.

<b>Examples:</b><br>
Searching `race:elf` will result in all articles that have the "race" option set to "elf".<br>
Searching `type:"player character"` will result in all articles that have the "type" option set to "player character".<br>
Searching `groups:[party "house lenora"]` will result in all articles that have the "groups" option set to "party" or "house lenora".<br>

## Combining Search Terms
You can combine multiple search terms. Articles will be searched for if any of the search terms apply. It is currently not possible to search for articles where all terms apply.

<b>Examples:</b><br>
Searching `Carac tag:pc groups:party` will result in all articles that have either "Carac" in their name, the "pc" tag, or the "groups" option set to "party".