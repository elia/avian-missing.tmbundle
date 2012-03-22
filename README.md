# Avian Missing

This is a collection of missing features from TextMate2-alpha.
This bundle includes:

### Save Project (⌃⌘S)

The save project command will now create a `.tm_properties` in the current file browser folder precompiled with `projectDirectory` set and an example `windowTitle`

**Default:**

```bash
projectDirectory = "$CWD"
projectName = "${projectDirectory/.*\///}"
windowTitle = "$TM_DISPLAYNAME     ☛${TM_SCM_BRANCH}     [${projectName}]"
```

### Character class indifferent completion (⎋)

TextMate 2 [introduced](http://blog.macromates.com/2012/clever-completion/) strict …err …clever completion, which will not cross boundaries between character classes anymore. For example in Ruby typing `au` and hitting `⎋` for autocompletion will not pick `:auto` or `@autocomplete` since they have a leading `:` and `@` and the belong to the *symbol* and *instance variable* character classes. 

This bundle reintroduces the TM1 behavior.


## Installation

```bash
mkdir -p ~/Library/Application\ Support/Avian/Bundles
cd !$
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
