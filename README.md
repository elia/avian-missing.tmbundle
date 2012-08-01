# Avian Missing

This is a collection of missing features from [TextMate 2.0 Alpha](http://blog.macromates.com/2011/textmate-2-0-alpha/).
This bundle includes:

## Save Project `⌃⌘S`

The save project command will now create a `.tm_properties` in the current file browser folder
precompiled with `projectDirectory` set and an example `windowTitle` featuring the
current scm-branch and the `$projectDirectory` basename

**Example:**
```
 application.rb     ☛master     [awesome-app]
```

This command also saves the project in the favorities (accessible with `⌘⇧O`).


## Character class indifferent completion `⎋`

TextMate 2 [introduced](http://blog.macromates.com/2012/clever-completion/) strict …err …clever completion, which will not cross boundaries between character classes anymore. For example in Ruby typing `au` and hitting `⎋` for autocompletion will not pick `:auto` or `@autocomplete` since they have a leading `:` and `@` and the belong to the *symbol* and *instance variable* character classes.

This bundle reintroduces the TM1 behavior.


## Cross tab completion `⌘;`

[RubyAMP](http://code.leadmediapartners.com/) used to have this.


## New File `⌃⌘N`

This command creates a new file in the current folder and presents a save dialog right away as in TM1 instead of opening the [dreadful](http://tm2tips.tumblr.com/post/16467488354/create-a-new-file-in-a-project-folder) TM2 *untitled* tab. The command is accessible also by control-clicking on the file browser.

_NOTE: don't hold your ⌘ or ⌃ because they can trigger other actions while the bundle is typing the current filename in the dialog_


## Open Project directory in Terminal `⌃⌥⌘T`

_NOTE: requires OSX Lion_

Opens the current project directory in the terminal (not really present in TM1, but useful anyway).


## Keep current file as reference `⌃⌥⌘L`

> …waiting for split panes

Outputs the current source into the bottom html pane, this makes the current file source visible while changing tabs.

Seems that most of the need for split panes is to keep one file as a reference, this solves this particular issue.


## Open the global `.tm_properties` with `⌥⌘,`

Tired of opening `.tm_properties` from the terminal or browsing to it by hand?

Now you can just hit `⌥⌘,` and bring up your alternative preferencies (from you the home folder).




<br><br>

## Installation

```bash
mkdir -p "~/Library/Application Support/Avian/Bundles"
cd "~/Library/Application Support/Avian/Bundles"
git clone git://github.com/elia/avian-missing.tmbundle.git
```


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


## Copyright

Copyright © 2012 Elia Schito. See MIT-LICENSE for details.
# Avian Missing