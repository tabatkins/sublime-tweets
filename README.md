# Sublime tweets

This repository contains a simple syntax-highlighting file
to help you compose tweets offline
in a real text editor
(specifically, Sublime Text 3),
then post them later in the actual Twitter interface.

It automatically counts characters for you,
including Twitter oddities like URLs and emoji,
and highlights when you go over the 280char limit,
just like in the Twitter interface.

## Installing

To install,
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

This *should* correctly match Twitter character counting,
including URLs, emoji, and CJK/etc characters.

I know that I didn't quite copy the current URL regex
for some strange corner cases,
like putting directional-override chars in,
but that shouldn't matter for virtually any real-world usage.
Regardless, I'll probably fix that properly at some point.