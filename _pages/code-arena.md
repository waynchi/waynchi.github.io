---
layout: page
permalink: /code-arena-old/
title: Code Arena
nav: false
nav_order: 100
---

This page is a WIP project. If you stumble across this page and are curious about our work, please email me.

Code Arena is an open source code AI coding assistant that provides paired autocomplete suggestions. Code Arena is **free** to use.

The goal of this project is to evaluate which language models provide the best coding assistance.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/code-arena-demo.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>

## Installation Instructions

1. Download the latest version [here](/assets/vsix/arena-0.0.13.vsix)
2. Open Visual Studio Code.
3. Go to the Extensions view (Ctrl+Shift+X).
4. Click on the "..." menu in the top-right corner of the Extensions view.
5. Select "Install from VSIX..." and choose the downloaded file.
6. Restart Visual Studio Code after installation.

If you’ve installed Code Arena before, please delete the ~/.code-arena folder to prevent any issues with new updates.

If installed successfully you will see Arena showing up on the bottom right corner of your window. 
When a completion is being generated, the check mark changes to a spinning circle.

## User Interface / How to Understand Your Completions

Code Arena adopts a slightly different user interface compared to a typical code completion.

1. Code Arena displays two completions, one on top of the other.
2. Code Arena repeats the same line prefix to keep the top and bottom outputs as similar as possible.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/code-arena-example.png" title="Code Arena Example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Accepting Suggestions
Press ```Tab``` to accept the top suggestion and ```Shift-Tab``` to accept the bottom suggestion.

## Code Arena Settings

Code Arena provides several settings. You can find all settings by searching for "arena" in your vscode settings.

| Setting | Description |
|---------|-------------|
| arena.enableTabAutocomplete  | Enable Arena's tab autocomplete feature. |
| arena.enableAutomaticTabAutocomplete&nbsp;&nbsp; | Enables automatic autocomplete suggestions while typing.  Turn off to force manual invocations. |
| arena.maxOutputLines | Limit the number of lines of code that can be outputted. Default is 5 lines. |
| arena.removeQueryDelay | Removes the delay before querying for a response. Unnecessary for most users as the delay from APIs dominates. Keeping this off helps reduce our operation costs. |
| arena.queryDelay | The delay (in seconds) before querying the server for a completion. |
| arena.displayCompletionIds | Display completion ids (next to the =====). This is used for debugging purposes. |

## Privacy

The code in your current file is sent to our servers and sent to various API providers. By default, we do not collect your code for research purposes; we only collect your vote for the leaderboard.
However, we log your code for the purposes of debugging. You can opt-out of this.

- To opt-in to data collection, please: WIP (we would really appreciate this!)
- To opt-out of logging entirely, please: WIP. Opting-out means any bugs you encounter will be non-reproducable on our end.

## Bug Reports

Please submit a bug report [here](https://docs.google.com/forms/d/1LiXtL2-VbOdTVybD9TUTlAhPzN9acGG7Y9NZ532C6pY/edit)

## Voting Visualizations

WIP

## Publication

WIP

## FAQ
Q: My tab isn’t working / Code Arena doesn’t work well with Copilot code completions!
A: Yes, Copilot code completions don't work with Code Arena as (a) they both use the completions API and (b) they both require use of the tab key. You don't have to disable all of Copilot; instead, if you click on the copilot icon in the bottom right corner, you should be able to disable their completions feature only.

Q: Code Arena is lagging my VSCode.
A: Please restart VSCode; it should fix itself in less than a minute after you restart the application. This should be fixed in the latest version, so if you are still experiencing this issue

Q: My Inline completions are not being generated?
A: Try a few times to ensure that it isn't due to cold start. Also, try restarting VSCode or triggering the suggestions manually.
Note that completions will not display if (a) you move away from the window or (b) the suggestions window (i.e. classic autocomplete) is showing.

Q: What is the expected response time for a completion?
A: Most completions should finish in around 1 second, although some may take up to 2 seconds. Some model APIs have high latencies and we are working with model providers to decrease latency.

Q: How do I trigger the inline suggestion manually?
A: There is a command called “Trigger Inline Suggestion” you can run. This is oftentimes much faster than waiting for an inline suggestion.

Q: My inline completions are still not being generated?
A: You can run the “Developer: Toggle Developer Tools” Command to see debug logs. You should see logs like the following which indicate the completions are being generated.


## Versions
- [Arena v0.0.13](/assets/vsix/arena-0.0.13.vsix)
- [Arena v0.0.12](/assets/vsix/arena-0.0.12.vsix)
- [Arena v0.0.11](/assets/vsix/arena-0.0.11.vsix)
- [Arena v0.0.10](/assets/vsix/arena-0.0.10.vsix)
- [Arena v0.0.9](/assets/vsix/arena-0.0.9.vsix)
- [Arena v0.0.8](/assets/vsix/arena-0.0.8.vsix)
- [Arena v0.0.7](/assets/vsix/arena-0.0.7.vsix)

## Changelog

### 0.0.13
- Bug fix: Model voting history now loads when the webview becomes visible.

### 0.0.12
- Model voting history persists across sessions

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

## Terms of Service 

WIP