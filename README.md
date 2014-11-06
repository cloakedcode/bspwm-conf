# bspwm-conf #

My beautifying of bspwm with pretty colorschemes.

(*Note:* If you're impatient to make your desktop beautiful, skip to the [How](#how) or [Installation](#installation) sections.

## What ##

This is my collection of scripts and config tweaks that make my desktop look like this:

![Pretty screentshot](https://raw.githubusercontent.com/cloakedcode/bspwm-conf/master/screenshot.png)

or this:

![Another beautiful shot](https://raw.githubusercontent.com/cloakedcode/bspwm-conf/master/screenshot2.png)

Actually, it changes everytime I login! It rotates through a number of colorschemes and photos, but those can be easily changed.

[UnixPorn](http://www.reddit.com/r/unixporn) provided inspiration and pieces of the panel/bspwmrc puzzle. Specifically [u-ra](https://github.com/u-ra/dotfiles) and [windelicato](https://github.com/windelicato/dotfiles), thanks for sharing!

## Why ##

Because drooling over screenshots of bspwm provides limited satisfaction. I want to have a usable desktop that looks beautiful, not just pictures of them.

I'm publishing this setup because I spent way too long hunting through UnixPorn trying to find a setup I liked, only to find copying their configs was either difficult or, once copied, hard to customize.

## How ##

Alright, here's the skinny, the low down:

 * [wp](https://github.com/everett1992/wp) generates colorschemes from photos ([Have some more!](http://chromecastbg.alexmeub.com/))
 * [wp_change](https://github.com/cloakedcode/bspwm-conf/blob/master/bspwm/wp_change) gets called from the autostart script and, chooses one of the wallpapers/colorschemes in wp upon login. This changes the .Xresources, in effect, and sets the background image. (It also changes the xfce4-terminal colorscheme if you're using that term emulator.)
 * `bar` picks up the colorscheme through the [config file](https://github.com/cloakedcode/bspwm-conf/blob/master/bspwm/panel/config) and substitutes the colors into the [conky config](https://github.com/cloakedcode/bspwm-conf/blob/master/bspwm/panel/panel_conky_cosmo)

## Installation ##

If you're going to install this on your machine, there are three things to be aware of:

 1. Make sure the autostart script is called from your `.xinitrc` or by your login manager
 2. Add some photos to `wp` so there are colors and photos to play with
 3. Modify the autostart script to fit your system (e.g. remove `connmand` if you're not using connman)

## Contributing ##

Please do! If you find something that makes bswpm customization easier/more flexible, I'd love to get a pull request.

Of course, if you find a bug or a foolish mistake, definitely submit a PR/issue.
