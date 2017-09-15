xsel is a wonderful thing.

On a mac you have utilities like `pbcopy` and `pbpaste` that can be used to manage the clipboard, making for some useful interactions within your epic one liners

Linux doesn't have those, but it does have a utility called `xsel` and _multiple "clipboards" (i.e. selections)_

Equivalents for the mac commands above are:

- `pbcopy` === `xsel --input --clipboard` or `xsel -ib` for short

- `pbcopy` === `xsel --output --clipboard` or `xsel -ob` for short

In addition to that, there's another commonly used behaviour with the primary selection (the place used when you highlight text and are then able to "paste" it by middle clicking)

`xsel --input --primary` or `xsel -ip` will put whatever text you want into that selection

`xsel --output --primary` or `xsel -ob` will return it

You can pipe input/output to these commands, in typical unix style, e.g.

`cat longfile.sql | xsel -ib`
