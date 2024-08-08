---
layout: page
permalink: /code-arena/
title: Code Arena
description: Code Arena
nav: false
nav_order: 100
---

# Code Arena

This page is a WIP project. If you stumble across this page and are curious about our work, please email me.

## Code Arena VSIX Extensions

Below you'll find links to download our VSIX extensions:

- [Arena v0.0.11](/assets/vsix/arena-0.0.11.vsix)

## Updates

### 0.0.11
- Added the ability to view the voted for model in the status bar (bottom bar).
- Added model voting history (computer icon on the activity bar; this is usually the left bar).
- Added a setting to toggle off.

### 0.0.10
- Added configuration to disable automatic tab autocompletions.
- Fixed a bug that delayed the query when invoking manually.

### 0.0.9
- Added configurations for query delay and max output lines.

### 0.0.8
- Added completion ids to the display. For debugging purposes only and should not be released fully.

### 0.0.7
- Switched to a more stable server. Anything before 0.0.7 is unstable.

## Installation Instructions

1. Download the desired VSIX file by clicking on the link above.
2. Open Visual Studio Code.
3. Go to the Extensions view (Ctrl+Shift+X).
4. Click on the "..." menu in the top-right corner of the Extensions view.
5. Select "Install from VSIX..." and choose the downloaded file.
6. Restart Visual Studio Code after installation.

If you’ve installed Code Arena before, please delete the ~/.code-arena folder to prevent any issues with new updates.

If installed successfully you will see Arena showing up on the bottom right corner of your window. 
When a completion is being generated, the check mark changes to a spinning circle.

## Accepting Suggestions
Press “Tab” to accept suggestion 1 (top) and “Shift-Tab” to accept suggestion 2 (bottom).

## FAQ
Q: My tab isn’t working / Code Arena doesn’t work well with copilot!
A: Yes, copilot doesn’t work with Code Arena as Code Arena takes over the tab key. Disable the extension and reload your vscode window.

Q: Code Arena is lagging my VSCode.
A: Please restart VSCode; it should fix itself in less than a minute after you restart the application. (Should be fixed in the latest version)

Q: My Inline completions are not being generated?
A: Note that it currently needs some time before completions start working (Reason unknown). If it doesn’t work at first, try a few more times and completions should start showing up.
Also, try restarting VSCode or triggering the suggestions manually.

Q: How do I trigger the inline suggestion manually?
A: There is a command called “Trigger Inline Suggestion” you can run. This is oftentimes much faster than waiting for an inline suggestion.

Q: My inline completions are still not being generated?
A: You can run the “Developer: Toggle Developer Tools” Command to see debug logs. You should see logs like the following which indicate the completions are being generated.

## Older versions
- [Arena v0.0.10](/assets/vsix/arena-0.0.10.vsix)
- [Arena v0.0.9](/assets/vsix/arena-0.0.9.vsix)
- [Arena v0.0.8](/assets/vsix/arena-0.0.8.vsix)
- [Arena v0.0.7](/assets/vsix/arena-0.0.7.vsix)