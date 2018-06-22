#Setting up SublimeREPL with Python3


First I use mac OS, so already have Python 2.7 and 3.6.
I use Sublime Text 3 like an editor, with SublimeREPL for console mode.
At this point, SublimeREPL has as default the version 2.7, this is wat I want to change for the 3.6 v.

I need to go in my Sublime Text editor to: `__Tools->Build System->New Build System__` and put the next lines:

	{ "cmd": ["python3", "-i", "-u", "$file"], "file_regex": "^[ ]File \"(...?)\", line ([0-9]*)", "selector": "source.python" } </code>

Then save it with a meaningful name like: python3.sublime-build (the extension for the building).

The last step to do is go to edit the __Main.sublime-menu__ file, it's located: `/Users/your_user/Library/Application Support/Sublime Text 3/Packages/SublimeREPL/config/Python`

Here you just need to put the number of the version 3 in some order, but I leave the example of my final file in a gist so you can check it:
https://github.com/jareacher/Baul/commit/38f74d1f8f6d6eaf6bd6a291d6065cd97b8fae15

And that's all! so simple I know but helps! Greetings.
