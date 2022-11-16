# What is Inner Source

This is a shot talk put together as quickly as I could. The goal is to explain what inner source is, why it's important, and what we should look to implement in an enterprise to achieve it.

## Just show me the deck

The _index.html_ file in the root of the repo should already be [hosted on GitHub Pages](https://froi.github.io/inner-source/). You can skip all the steps and go straight to enjoying the slide deck.

To navigate the deck use your keyboard's arrow keys. Take a look at the direction you want to go in by following the arrows in the lower right corner of the deck.

If you want even more options type `?` and you'll get a fancy list with all the options you have. For example, press `S` to go into the speaker view and get a look at the speaker notes :wink:

## The repo

All slides are done in Markdown. I'm using Pandoc to "build" the slides into a [Reveal.js](https://revealjs.com/) deck that is hosted on [GitHub Pages](https://pages.github.com/)!

- __index.html:__ The compiled slide deck
- __myslides.md:__ The deck's slides in Markdown format

## Compiling the deck

Before you start you will need to [install Pandoc](https://pandoc.org/installing.html) on your computer or use Docker to execute the tool.

Once you have Pandoc installed, clone this repo

```shell
~
➜ git clone https://github.com/froi/inner-source.git
```

Now that you have it cloned move into the created folder and from the root of the project run Pandoc!

```shell
inner-source on  main [✘!?]
➜ pandoc -t revealjs -s -o index.html myslides.md -V theme=black
```

Now you can just open _index.html_ in your browser and enjoy the deck!
