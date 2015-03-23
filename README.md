# Aurora

'Aurora' is my custom vim color scheme, modeled closely after the [Solarized](http://ethanschoonover.com/solarized)
Dark color scheme. It was designed using Solarized Dark as a base starting point,
but it diverges according to the following design principles:

 * **Compatibility/consistency between gvim and terminal vim.**

   Solarized doesn't tend to work so well using xterm 256 colors, possibly
   because its color choice is so specialized. Initially, my custom color
   scheme (that would eventually turn into Aurora) was an attempt to mimic
   Solarized, but with the constraint of only using xterm colors. As much as
   possible, I've strived to keep the 24-bit gvim colors identical, or at
   least very similar, to the color choices used for the terminal color scheme.

 * **Emphasis on higher contrast color groupings.**

   My biggest complaint with Solarized Dark is that, when editing code, the 
   color choice makes various syntax elements blend together too much. The
   most notable example is the color of comments: a dark gray that makes them
   very easy to gloss over when scanning through code.

   Aurora, on the other hand, emphasizes contrast between major syntactical
   elements, e.g. comments, identifiers, and keywords. This makes it much
   easier to recognize and visually group together syntactical features while
   scanning through code.

 * **Harmonious color choices.**

   While I do not profess to know much about formal color theory, I chose
   these particular colors in an attempt to keep them 'harmonious' with each
   other. By that, I mean that this color scheme is heavily centered around
   blue/green tones, accented by light grays and dark turquoises. There was no
   formal process or method to my selection; I simply hand-tweaked until I
   found the colors aesthetically pleasing and, to my eye, balanced.

## Screenshots

![C](http://i.imgur.com/s4ZROsQ.png)

For more, see the [screenshots page](https://github.com/henrybw/vim-colors-aurora/wiki/Screenshots) on the wiki.

## Installation

1. If you have [Pathogen](https://github.com/tpope/vim-pathogen), then you can
   simply clone this repo into your `~/.vim/bundle`:

        $ cd ~/.vim/bundle
        $ git clone https://github.com/henrybw/vim-colors-aurora

    (This process should theoretically also work for Vundle and other similar
     vim plugin managers.)

    If you don't use a plugin manager, then you can add the relevant file to
    your `.vim/colors` directory:

        $ mkdir -p ~/.vim/colors
        $ cd vim-colors-aurora/colors
        $ mv aurora.vim ~/.vim/colors/

2. Modify your .vimrc:

   Add the following lines to your `~/.vimrc` file to enable Aurora:
   
         syntax on
         colorscheme aurora
   
   NOTE: To have the terminal colorscheme work properly, you may need to also add
   the following lines to your .vimrc:
   
         set t_ut=
         set t_Co=256
