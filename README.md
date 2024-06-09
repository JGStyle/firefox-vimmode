### What is this?

This is a clone of firefox. It aims to make browsing with firefox fast by integrating vim like keybindings to firefox.
The ultimate goal is to be able to fully control the browser with just the keyboard.

### why?

> Why don't you just use extensions like Vimium

There are numerous extensions that try to mimic vim like funcitonality in the browser.

The problem is that extensions are very limited. They can't trigger certain browser-level features
- No full history control
- Browser search
- Don't work in the browsers PDF viewer
- Don't work in the browsers settings
- Only work in an active website
- can't add browser level UI for example to show the current vim moe

because of that they have to either akwardly reimplement the feature with a javascript work around (like a custom search, or a custom url bar) or they just don't support the feature
To truly get a vim like experience you need browser level control.

> But there are already Browsers that try to do this

That's true but the options on the market don't fulfill the requirements that I need:

- I want the browser to be gecko engine based because Mozilla is non-profit and an advocate of the open web. There are enough chromium like browsers.
- the browser should support ARM architecure (Apple M1 to be specific) 
- the browser should look somewhat modern
- thr browser should support the widely available extensions
- the browser should support modern HTML, CSS, JS Features

This is why browsers like qutebrowsers don't qualify in my opinion


### Supported Keybinds

Normal Mode:
- I: instantly go into the URL bar and switch into insert mode
- i: go into insert mode and enter the next <input> field on the open webpage (not ready yet)
- t: open a new tab 
- x: close the open tab (or window if last tab)
- j: scroll down
- k: scroll up
- J: go back in the browser history
- K: go forward in the browser history
- r: reload page
- R: reload page and skip cache
- /: open browser level search and enter insert mode
- n: go to the next search result
- N: go to the previous search result
- u: browser level undo (not ready yet)
- w: open a new window
- W: open a new private window
- Esc: defocus active input and enter normal mode

Other:
- C-p : enter special passthrough mode that will pass all keys to the browser, useful for stuff like browser games
- C-r : browser level redo


### how to use

as of right now there are no official realeases.
As soon as the project is ready, I will start looking into it.
If you want to use it already. go through the following steps:

- follow the offical Mozilla Steps on how to clone firefox
- replace the files in the firefox/browser that have the same names and folder structure as the on in my repo.hat
    For Example, replace the firefox/browser/base/content/browser-init.js with the file from this repo.
- build and run the changed browser using `./mach build ; ./mach run`



