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

### Requirements

You need to **Enable access for assistive devices** in order to make it work:

- Open your **System Preferences**
- [Open **Accessibility**](https://f.cloud.github.com/assets/1051/120814/4f8e36a8-6d3d-11e2-9803-d7e4f9c379d9.png)
- [Tick **Enable access for assistive devices**](https://f.cloud.github.com/assets/1051/120815/51f67d6a-6d3d-11e2-8b9a-7e983459ea55.png)

### Caveats

- Don't hold your ⌘ or ⌃ because they can trigger other actions while the bundle is typing the current filename in the dialog_
- Some users are reporting a missing `TM_SUPPORT_PATH` variable, 
  if it's the case try adding to your global `.tm_properties` (or to _Preferences→Variables_ if you prefer):

      TM_SUPPORT_PATH = "~/Library/Application Support/TextMate/Managed/Bundles/Bundle Support.tmbundle/Support/shared"



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



## Strip trailing whitespace on save

Just add `TM_STRIP_WHITESPACE_ON_SAVE = true` to your `.tm_properties`.
Ending newline fix is included.


<br><br>

## Installation

```bash
mkdir -p ~/Library/Application\ Support/Avian/Bundles
cd ~/Library/Application\ Support/Avian/Bundles
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
