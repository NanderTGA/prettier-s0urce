# prettier-n0urce

NanderTGA's fork/branch of prettier-s0urce.

All previous, current, and future versions of prettier-s0urce are licensed under the GNU GPL v3.

## About & Why

This fork of prettier aims to merge the multiple existing forks/branches into one awesome prettier.
While main prettier (Xen0o2's) and d0t's fork currently just go around copy-pasting each other's changes,
I use git's merging features to do it properly and not miss out on any changes or details.
That does come with the possibility of a merge accidentally breaking stuff, but I try to be careful.
I also aim to rewrite some code that I think could be better.

The downside? I'm not the fastest person and I'm currently behind on both Xen0o2's and d0t's branches, this is a work-in-progress after all.

## Installation

Convinced? Alright, welcome to the squad.
Remember, it doesn't matter whether you use prettier or not and which variant you choose. No need to fight ;)

There are 4 ways to launch prettier (these instructions can apply to any variant):

### The recommended way

Use your favorite userscript manager. This solution automatically launches prettier every time you hop on s0urce and automatically checks for updates. When it finds a newer version available, it will ask you if you want to update.

In case you don't have a userscript extension yet, we recommend [ViolentMonkey](https://violentmonkey.github.io/) because it is free/libre software, while the popular extension TamperMonkey is not. Do note that it doesn't support mobile firefox at the moment, so you may have to use TamperMonkey instead there.

<details>

<summary>Browser rant (TLDR ViolentMonkey doesn't support Google Chrome and you should use Firefox instead for multiple reasons)</summary>

Do note that ViolentMonkey does not support Google Chrome, but you shouldn't be using that hot piece of garbage browser anyway. It does not support extensions on the mobile version, Google sabotaged ad/content blockers like uBlock Origin with the creation of ManifestV3 and they [do not care about protecting your privacy](https://privacytests.org).
Instead, you should use a less sketchy browser like [Mozilla Firefox](https://firefox.com), which has support for some extensions on mobile and seems to care more about protecting your privacy. Mozilla is not perfect either though, so there are forks like [Librewolf](https://librewolf.net) and [IronFox](https://ironfoxoss.org) that aim to further improve upon their work.

I should probably also mention that other chromium-based browsers are usually less sketchy and some of them do feature support for extensions on mobile,
and others like [Cromite](https://cromite.org) feature ad blocking and privacy improvements. I recommend Firefox and its forks mainly because of Google's monopoly on the browser market with chromium and the fact that they abused this monopoly by pushing ManifestV3.

</details>

Apart from the above browser rant, here are some detailed instructions:

- Install a userscript extension like ViolentMonkey (see above)
- Open one of these links (preferably in a new tab): [prettier-n0urce (NanderTGA)](https://raw.githubusercontent.com/NanderTGA/prettier-s0urce/main/prettier-s0urce.user.js) or [prettier-s0urce (Xen0o2)](https://raw.githubusercontent.com/Xen0o2/prettier-s0urce/main/prettier-s0urce.user.js) or [prettier-d0urce (d0t)](https://raw.githubusercontent.com/d0t3k1/d0t-s0urce-prettier/main/d0urce-prettier.user.js)
- If your userscript extension is working, it'll show a screen with some buttons. Click the button that reads `Install`.
- Go back to s0urce and refresh the tab. After you press play, you should notice prettier launching.
- You can now close the other tabs.

### The copy-paste way

If you don't have a userscript manager and can't install one for whatever reason, but you do have access to devtools, this works fine as well. You do have to manually go copy the code from github every time to then paste it in the console.

Here are some more detailed instructions:

1. Open one of these three links in a new tab directly, then press `Ctrl + A` and `Ctrl + C` to copy the entire file: [prettier-n0urce (NanderTGA)](https://raw.githubusercontent.com/NanderTGA/prettier-s0urce/main/prettier-s0urce.user.js) or [prettier-s0urce (Xen0o2)](https://raw.githubusercontent.com/Xen0o2/prettier-s0urce/main/prettier-s0urce.user.js) or [prettier-d0urce (d0t)](https://raw.githubusercontent.com/d0t3k1/d0t-s0urce-prettier/main/d0urce-prettier.user.js)
2. Go back to the s0urce tab, and press F12 or `Ctrl + Shift + I`. This will open the developer tools. In the panel or window that appears, click on the console tab somewhere at the top.
3. In this console tab, click somewhere on the bottom of the window to make sure you can type in there.
4. Press `Ctrl + V` to paste the code and press enter to run it. If you're on some chromium-based browser, pasting code may not work. If this happens, type `allow pasting;` and press enter, then try pasting again.
5. If you did everything correctly, you should notice prettier launching. You can now close the github page and the developer tools; the button to close devtools is usually in the top right corner.

### The Bookmarklet way

A bookmarklet is a bookmark that runs javascript on the current page. Handy, right?
If you think this is cool you might want to check out [this way cooler bookmarklet](https://kickassapp.com) the next time you're bored.

So here are the instructions:

1. Drag one (or multiple) of these links onto your bookmarks. [prettier-n0urce (NanderTGA)](javascript:fetch%28%22https%3A//raw.githubusercontent.com/NanderTGA/prettier-s0urce/main/prettier-s0urce.user.js%22%29.then%28response%20%3D%3E%20response.text%28%29%29.then%28eval%29) or [prettier-s0urce (Xen0o2)](javascript:fetch%28%22https%3A//raw.githubusercontent.com/Xen0o2/prettier-s0urce/main/prettier-s0urce.user.js%22%29.then%28response%20%3D%3E%20response.text%28%29%29.then%28eval%29) or [prettier-d0urce (d0t)](javascript:fetch%28%22https%3A//raw.githubusercontent.com/d0t3k1/d0t-s0urce-prettier/main/d0urce-prettier.user.js%22%29.then%28response%20%3D%3E%20response.text%28%29%29.then%28eval%29)
2. Whenever you want to run prettier, click on one of these bookmarks. It doesn't matter whether you do this before or after clicking play. Make sure you're on the s0urce tab when clicking the bookmark though, otherwise nothing will happen. When you click the bookmark, you should notice prettier launching.

### When all else fails... THE MISSION POSSIBLE WAY

This cool method uses a bug in the terminal to run prettier.
You can actually run any other javascript code using this method too.
I've used this method countless of times myself to run prettier on my school chromebook.

Very big thank you to Nelumbo for finding this very useful bug!

1. Start hacking someone
2. Paste this snippet in the terminal and press enter: `<a onclick="eval(prompt())">`
3. Click the white text that appears in the terminal. You'll now get a popup. You can paste any javascript here and click OK to execute it.
4. We're gonna load prettier using this, so paste this snippet in the popup and click OK: `fetch("https://raw.githubusercontent.com/NanderTGA/prettier-s0urce/main/prettier-s0urce.user.js").then(response => response.text()).then(eval)`
    - Want to load Xen0o2's prettier instead? Paste this instead in the last step: `fetch("https://raw.githubusercontent.com/Xen0o2/prettier-s0urce/main/prettier-s0urce.user.js").then(response => response.text()).then(eval)`
    - Want to load d0t's prettier instead? Paste this instead in the last step: `fetch("https://raw.githubusercontent.com/d0t3k1/d0t-s0urce-prettier/main/d0urce-prettier.user.js").then(response => response.text()).then(eval)`
5. You should now notice prettier launching. MISSION POSSIBLE!

## My Local Setup

Branches:

- `main` branch, which is where the end result ends up
- `d0urce-main` branch: this is the main branch of d0t's fork but with one extra commit that renames `d0urce-prettier.user.js` to `prettier-s0urce.user.js` so git merge can work

Remotes:

- `upstream`: [Xen0o2's prettier repository](https://github.com/Xen0o2/prettier-s0urce)
- `origin`: this repository
- `d0urce`: [d0t's prettier repository](https://github.com/d0t3k1/d0t-s0urce-prettier)

To merge from Xen0o2's prettier repository, I merge from the `upstream` remote into the `main` branch.
To merge from d0t's prettier repostiroy, I first pull those commits into `d0urce-main`, then merge from that branch into `main`.

## TODO

- setup eslint
- commit "new command system" line 1758 removed inventory index numbers
  - re-add using an option/setting (disabled by default ig)

### Notes

- Do not merge d0urce v1.8.0, I wrote my own profile links feature instead (kinda wip, need to add a MutationObserver to the target list)
- Do not merge "fix: tampermonkey issue" eithe, it removes window snapping, but I already moved that to an option disabled by default
