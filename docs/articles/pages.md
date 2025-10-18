<div class="imgContainer"><img src="../../img/article/pages.png"></div>
Each article can contain one or more pages, which are essentially text documents.

The pages of an article will show up below the article's title (or linked documents section, if configured). The displayed page is highlighted, and you can navigate to another page by pressing the page's title.

If there is only 1 page, the page title will not be displayed.

To make any changes to pages the article will need to be in [edit mode](./articles.md#playedit-mode).
<div class="clear"></div>

While in edit mode, you have access to the following buttons:
<div class="imgContainer"><img src="../../img/article/createDeletePages.png"></div>

| Button                                        | Action                                                            |
|-----------------------------------------------|-------------------------------------------------------------------|
| :material-dots-square:<br>Or selected icon    | Opens the [Icon Picker](#icon-picker) to add an icon to the page  |
| :fontawesome-solid-eye:                       | Hides or unhides the page                                         |
| :fontawesome-solid-key:                       | Makes or unmakes the page secret                                  |
| :fontawesome-solid-trash:                     | Deletes the page                                                  |
| :fontawesome-solid-plus:                      | Creates a new page                                                |

Additionally, you can perform the following actions:

* <b>Reordering Pages</b>: You can reorder pages by dragging one page button onto another
* <b>Changing a Page Title</b>: Click the title to select the textbox, and write the new name

## Text Editor
<div class="imgContainer"><img src="../../img/article/textEditor.png"></div>
The Worldbuilder text editor is almost the same as the core Foundry VTT text editor, as used by journal entries.

Only features unique to Worldbuilder will be discussed here.

### Saving Text
Any text written in the text editor will be saved in the following situations:

* By pressing the :fontawesome-solid-floppy-disk: icon
* When changing [modes](./articles.md#playedit-mode)
* When you close the article
* Every 30 seconds

### Inserts
Worldbuilder allows you to insert different kind of buttons, widgets, or other elements into the page. See [here](#page-inserts) for the different kind of inserts and how to configure them.

## Page Inserts
<div class="imgContainer"><img src="../../img/article/pageInserts.png"></div>
Page inserts are either buttons or embedded elements that (usually) can be interacted with.

You could, for example, insert a button to open a different article, or insert an interactive [map](../widgets/map.md).

There are 3 ways to add page inserts to your page:

1. Dragging a Foundry document, worldbuilder article, or worldbuilder widget onto the page. This will place the insert at the location of the cursor.
2. Press the :fontawesome-solid-globe: icon on the page editor toolbar, select the type of insert, and fill in the details in the popup.
3. Manually entering the widget using the correct syntax (see below).

### Insert Syntax
The following syntax is used for page inserts:

```(prefix)(insert type)[data]{label}```<br>
examples:<br>
```
@WB[characters.8GZOzo0RbPZ0iErU]{Carac Farlight}
@IMG[image.webp]{Label}
!WIDGET[map.qvTYLJfSJCpIiGoX]
```

<b>Prefix:</b><br>
The 'prefix' designates whether the insert should be a button (`@`) or an embedded element (`!`).
<div class="imgContainer"><img src="../../img/article/pageInserts-prefix.png"></div>
Take the following example, which will create a button with label "Video Button", which will open a popup to play the video if clicked. Below that, a video element is inserted.
```
@VIDEO[video.webm]{Video Button}
!VIDEO[vide.webm controls width:300 height:300 float:left]
```

<b>Type:</b><br>
The type determines the kind of insert. See the table [below](#insert-types) for the different insert types.

<b>Data:</b><br>
Data consists of, at least, the UUID of an article, widget, document, etc, and optional styling data.<br>
The styling data takes HTML style tags, such as:

```
width:100px //set the element width to 100 pixels
height:50px //set the element height to 50 pixels
color:red //set the text color to red
background-color:#00FF00 //set the background color to #00FF00 (green)
```

For example, the following insert will create a button to open a Worldbuilder document with red background and green text:
```
@WB[characters.8GZOzo0RbPZ0iErU background-color:#FF0000 color:#00FF00]{Carac Farlight}
```

Style tags are separated with a space. No space is allowed between the tag and value, so `width:100px` is fine, `width: 100px` is not.

See the table below for more optional other fields.

<b>Label:</b><br>
Only for button inserts.<br>
The label that will be displayed on the button.

### Insert Types

| Type  | Description  |Syntax    | Data Options  |
|--|--|--|--|
| Foundry document button       | Button that opens a Foundry document        | `@UUID[documentUuid]{label}`   | Style tags    |
| Worldbuilder article button   | Button that opens a [Worldbuilder article](../articles/articles.md)    | `@WB[articleUuid]{label}`   | Style tags    |
| Worldbuilder widget button    | Button that opens a [Worldbuilder widget](../widgets/widgets.md)    | `@WIDGET[widgetUuid]{label}`   | Style tags    |
| Worldbuilder tab button       | Button that opens a [Worldbuilder tab](../mainApplication/mainApplication.md#navigating-through-the-app)        | `@TAG[tabName]{label}`    | Style tags    |
| Worldbuilder tag button       | Button that opens a [Worldbuilder tag](../tags.md)        | `@TAG[tagName]{label}`    | Style tags    |
| Image button                  | Button that opens an image popup             | `@IMG[imageUrl]{label}`   | Style tags    |
| Video button                  | Button that opens a video popup             | `@VIDEO[videoUrl]{label}` | Style tags    |
| Link button                   | Button that opens an URL     | `@URL[Url]{label}`        | Style tags    |
| Worldbuilder widget insert    | Embeds a [Widget](../widgets/widgets.md)       | `!WIDGET[widgetUuid]`         | Style tags    |
| Video insert                  | Embeds a video            | `!VIDEO[videoUrl]`        | Style tags<br>`controls`: show video controls<br>`loop`: loop video    |
| PDF insert                    | Embeds a PDF          | `!PDF[pdfUrl]`            | Style tags    |
| Icon insert                   | Embeds an icon                          | `!ICON[fontAwesomeIcon]`  | Style tags  |

## Secrets
<div class="imgContainer"><img src="../../img/article/pageSecrets.png"></div>
[Secrets](./articles.md#secrets) are parts of an article that are only visible to selected users.

You can make paragraphs secret by selecting the paragraph, then clicking the left-most option in the toolbar, selecting Block and then Secret.

You can also create a secret block first using the same method, and then filling it with text.
<div class="clear"></div>

## Icon Picker
<div class="imgContainer"><img src="../../img/article/iconPicker.png"></div>
The Icon Picker provides a way to search for and select [FontAwesome](https://fontawesome.com/) icons.

You can search for icons with the search bar and select how the icon is displayed (solid, regular, light, thin or duotone).

Click one of the icons to select it, then press the Select button.
