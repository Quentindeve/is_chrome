# Is this app Chrome ?

These days, developers experience has been prioritized over user experience. Despite both not being incompatible, too lazy companies are using big frameworks like CEF, Electron, NW or Node. All these frameworks have a common point: they use either [Chromium](https://www.chromium.org/chromium-projects/) or [Node](https://nodejs.org/en) to function.

# Why is it so bad ?

All these frameworks use [JavaScript](https://developer.mozilla.org/fr/docs/Web/JavaScript), a language originally made for the Web. The JavaScript problem is that **it is terrible**, both for developer experience and performances. But because it is **the only usable programming language in the browser**, many of us know it.

Companies, in order to not take time learning its developers good technologies, decided to create some frameworks that just ship **ENTIRE WEB BROWSERS**, with their known poor performances, to just enable developers to write "native", desktop applications using web technologies: HTML, CSS and JavaScript.

It results in poor-written applications with bad performances.

# How to catch'em ?

There is some techniques to find them:

## Is it ultra slow ?

If the app is insanely slow for its purpose, i.e editing a text file, you probably found a Chrome-based app. JavaScript frameworks have insanely terrible performances for any I/O operations.

## Can I open dev tools on it ?

This one is pretty blattant: Try Ctrl+Shift+I on the app. If it opens you Chrome's developer tools, you found one. This isn't a great test because developers can disable it.

## Does it have any Chrome-related files ?

If the app's root contains files listed in ``blacklist.txt``, it is for sure a Chrome-based app. Note that this blacklist is non-exhaustive.