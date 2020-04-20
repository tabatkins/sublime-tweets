# Sublime tweets

This repository contains a simple syntax-highlighting file
to help you compose tweets offline,
in a real text editor,
then post them later in the actual Twitter interface.

## Installing
To use,
just save the `Tweets.sublime-syntax` file
into your Sublime Text packages;
by default,
this is probably located at `~/.config/sublime-text-3/Packages/User/`.
You can just save the file directly into that folder,
or make a `Tweets` folder for it,
if you prefer to organize that way.

## Activating

Once saved to your Packages folder,
you can activate it like any other syntax highlighter,
from the menu in the lower right corner.
It's also automatically applied to any file with the `.tweet` or `.tweets` extension.

## Use

In a Tweets-highlighted file, just type out your tweet.
Once you pass 280 characters
(including newlines!),
the overflow will be highlighted as "invalid" text;
your colors file should have something appropriate.

You can compose multiple tweets in one file
by separating them with a line containing 4 or more `-` characters;
after that the count will reset,
letting you compose a tweetstorm all at once.

## Caveats

This does not currently implement fully-correct Tweet character counting;
in particular, if you use emoji or CJK characters,
they'll be counted as a single character,
but Twitter will count them against your length as double,
so you won't actually have as much length as the highlight indicates.

It **does** implement the url-matching that Twitter uses, however,
so those'll be counted correctly against your total length.

Patches welcome,
if I don't get to it myself!