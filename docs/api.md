The following functions can be useful, for example, to control Worldbuilder using macros:

### Open the Worldbuilder app
```js
worldbuilder.api.open(tab); //"tab" is an optional tab name

//Tab names: "home", "favorites", "sessions", "quests", "characters", "groups", "creatures", "locations", "objects", "other", "widgets", "tags", "settings"
```

### Toggle the Worldbuilder app open/close
```js
worldbuilder.api.toggle(tab); //"tab" is an optional tab name

//Tab names: "home", "favorites", "sessions", "quests", "characters", "groups", "creatures", "locations", "objects", "other", "widgets", "tags", "settings"
```

### Open a specific tab
```js
worldbuilder.api.openTab(tab); //"tab" is the name of the tab to open

//Tab names: "home", "favorites", "sessions", "quests", "characters", "groups", "creatures", "locations", "objects", "other", "widgets", "tags", "settings"
```

### Open article
```js
worldbuilder.api.openArticleApp(uuid); //"uuid" is the uuid of the article
```

### Open tag config
```js
worldbuilder.api.openTagApp(tag); //"tag" is the tag name
```

### Download logs
```js
worldbuilder.api.downloadLogs(all); //"all" is an optional (boolean) value to download all logs (if true), otherwise it will download the log for the current session
```