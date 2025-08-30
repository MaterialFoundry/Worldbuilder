To get started using Worldbuilder, please follow these steps:

1. [Check the module's requirements](#requirements)
2. [Link your Patreon account to your Foundry account](#linking-a-patreon-account)
3. [Install and enable the module](#module-installation)
4. [Configure the module](#module-configuration)
5. Learn about the Worldbuilder [application](./mainApplication/mainApplication.md), [articles](./articles/articles.md), [tags](./tags.md) and [settings](./settings.md)

## Requirements
To get Worldbuilder to work, you need:

* [Foundry VTT](https://foundryvtt.com/)
* A subscription of the [Material Foundry Patreon](https://www.patreon.com/materialfoundry) at the "Material Apprentice" tier or higher.

!!! info "Pre-Release"
    For the pre-release version of Worldbuilder, any non-free Material Foundry Patreon subscription is fine.

## Linking a Patreon Account
!!! info "Pre-Release"
    For the pre-release version of Worldbuilder, any non-free Material Foundry Patreon subscription is fine.<br>
    You also do not have to link your Patreon account to your Foundry account, so you can ignore this section. Worldbuilder will not show up under your subscriptions page (see below).<br>
    Instead, a manifest URL is provided on Patreon which you can use to install the module.

Worldbuilder is a premium module that requires a subscription to the [Material Foundry Patreon](https://www.patreon.com/materialfoundry) at the 'Material Apprentice' tier or higher.<br>
As a patron you can gain access to the module by linking your Patreon account to your Foundry account:

1. Log in on the [Foundry VTT website](https://foundryvtt.com/)
2. Edit your profile [here](https://foundryvtt.com/me/edit)
3. Link your Patreon account at the bottom of the page if you haven't already
4. Verify that Worldbuilder shows up under your [subscriptions](https://foundryvtt.com/me/subscriptions). If it doesn't appear as expected under the "Subscribed Content" page of your user profile, you may need to Refresh your Patreon link

## Module Installation
!!! info "Pre-Release"
    For the pre-release version of Worldbuilder a manifest URL is provided on Patreon which you can use to install the module. To install, look for the "Installing via Manifest URL" section in the link below.

You will need to install and enable Worldbuilder by following [this guide](https://foundryvtt.com/article/modules/).

## Module Configuration
After [installing and enabling](#module-installation) Worldbuilder, you might have to do some configuration before you can start using the module.

### User Permissions
Unless your server is on [the Forge](https://forge-vtt.com/) (see [here](#the-forge) for more info for Forge users), users will not need extra user permissions to view Worldbuilder articles (besides the article's [ownership settings](./articles/articles.md#ownership)). However, to create or edit articles, your users will need the "Upload New Files" permission. 

This permission is usually enabled for all user roles, except for "Player". If this is the case, Worldbuilder will detect this and show a popup where you can change these settings.<br>
You can also change them by going to the "Game Settings" sidebar tab, clicking "Configure Settings", and then "Open Permission Configuration".<br>
It is not required to grant this permission if you do not want specific users to be able to create or edit articles.

### The Forge
Due to the way the Forge handles user data, there are some things you have to do if you want your players to have access to your Worldbuilder data, and there are some limitations.

#### Forge Configuration
1. Make sure you run Worldbuilder at least once
2. Log into the Forge and go to your [Assets Library](https://forge-vtt.com/assets/browse).<br>There should be a "worldbuilder" folder, if not, go back to step 1
3. Hover over the "worldbuilder" folder and press the :fontawesome-solid-share-nodes: button, which opens a popup
4. Set Permissions to "Read Assets, Write Assets"
5. Set "Key name" to a name that's unique to your world. If you leave it set to "worldbuilder" and one of your players play in another game that uses Worldbuilder, there might be file conflicts. Something like "worldbuilder-[gameName]" could work
6. Click "Share Folder"
7. Let your players log into the Forge, then send them to the link.<br>Tip: If you've previously made an API key, you can find the Share Url [here](https://forge-vtt.com/account#api)
8. Open Worldbuilder, go to the [settings tab](./settings.md)
9. Under "Data Management" you will find "Forge Key Name" (if you're the GM), fill in the "Key name" used in step 5

You should be set to go!

#### Forge Limitations
When you make changes, for example, to an article, an updated file is sent to the Forge servers. If you then refresh too soon, the changes you've made might seem to have been lost, because it takes some time for the Forge servers to respond with the updated file.

Don't worry, your data is probably fine! If you refresh after a few minutes all should be fine.
