---
title: Design Best Practices
date: 2019-06-02T00:00:00-00:00
subsection: Web App Plugins
weight: 0
---


### Actions that apply to specific Channels
- Recommendation: Have your plugin register the actions to [the channel header](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerChannelHeaderButtonAction). This makes it quickly accessible by users and actions apply to the channel they're viewing. 
- Example:  Zoom meeting posts to a channel

![Custom Channel Header Button](/img/extend/bp-channel-header.png)

You can additionally [register a slash command](https://developers.mattermost.com/extend/plugins/server/reference/#API.RegisterCommand) on the server-side to take channel-specific actions.
- Example: Jira project subscriptions to a channel

![Slash Command](/img/extend/bp-slash-command.gif)


### Actions that apply to specific messages
- Recommendation: Have your plugin register a [post dropdown menu component](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerPostDropdownMenuComponent) with some text, icon and an action function. This adds your action to the "More Actions" post menu dropdown for easy discovery.
- Examples: Create or attach to Jira issue from a message; copy a message to another channel; report an inappropriate message

![Post Dropdown Menu](/img/extend/bp-post-dropdown-menu.png)

### Actions related to files or images
- Recommendation: Have your plugin register a [file upload method](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerFileUploadMethod) with some text, icon and an action function. This adds your new action to the file upload menu.
- Examples: File sharing from OneDrive or GDrive; Draw plugin for sketches

![File Upload Action](/img/extend/bp-file-upload.png)


### Actions that apply to specific teams
- Recommendation: Have your plugin register [left sidebar header component](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerLeftSidebarHeaderComponent) with some text, icon and an action function. This adds your action above your team's channels in the sidebar.
- Examples: Trello kanban board plugin, Github Plugin

![post dropdown menu](/img/extend/bp-left-sidebar-header.png)

### Quick links or status summaries of workflows
- Recommendation: Have your plugin register a [bottom team sidebar component](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerBottomTeamSidebarComponent). This adds icons to the lower left corner of the UI.
- Examples: GitHub sidebar links with summary of outstanding reviews or unread messages; ServiceNow incident status summary

![post dropdown menu](/img/extend/bp-bottom-team-sidebar.png)

### Global actions that can be taken anywhere in the server and not directly related to teams, channels or users
- Recommendation: Have your plugin register [main menu action](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerMainMenuAction) with some text, icon for mobile, and an action function. This adds your action to the Main Menu. You can additionally [register a slash command](https://developers.mattermost.com/extend/plugins/server/reference/#API.RegisterCommand) on the server-side.
- Examples: Share feedback plugin in Main Menu; /jira slash commands for quick actions

![post dropdown menu](/img/extend/bp-main-menu-action.png)

### Actions that apply to specific users
- Recommendation: Have your plugin register a [popover user actions component](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerPopoverUserActionsComponent). This adds your action button to the user profile popover.   
- Examples: ..

![popover user actions component](/img/extend/bp-user-popover.png)

### Display custom information on a user profile
- Recommendation: Have your plugin register a [popover user attribute component](https://developers.mattermost.com/extend/plugins/webapp/reference/#registerPopoverUserAttributesComponent). This adds your custom attributes to the user profile popover. 
- Examples: Custom User Attributes plugin

![popover user attribute component](/img/extend/bp-user-attributes.png)

### Actions related to emoji and GIFs
- Recommendation: Have your plugin add a component to the emoji picker. This is not yet supported, but some [work had previously started](https://github.com/mattermost/mattermost-server/issues/10412#issuecomment-481776595) with the issue currently opened as Help Wanted.
- Examples: Bitmoji plugin; GIFs via Giphy or Gfycat
