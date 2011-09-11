# Cheats for Cheats_fu

## Description:

[Cheat_fu](http://cheat-fu.heroku.com/) cheat sheets repo.

## Screenshot

![Screenshot at flick](http://farm6.static.flickr.com/5016/5517136146_624976a477_z.jpg)

[Screenshot at flick](http://www.flickr.com/photos/30142618@N02/5517136146/)

## Man Pages Background ( [by rtomayko](https://github.com/rtomayko/ronn) )

Some think UNIX manual pages are a poor and outdated form of documentation. I
disagree:

- Manpages follow a well defined structure that's immediately familiar. This
  gives developers a starting point when documenting new tools, libraries, and
  formats.

- Manpages get to the point. Because they're written in an inverted style, with
  a SYNOPSIS section followed by additional detail, prose and references to
  other sources of information, manpages provide the best of both cheat sheet
  and reference style documentation.

- Historically, manpages use an extremely -- unbelievably -- limited set of
  text formatting capabilities. You get a couple of headings, lists, bold,
  underline and no more. This is a feature.

- Although two levels of section hierarchy are technically supported, most
  manpages use only a single level. Unwieldy document hierarchies complicate
  otherwise good documentation. Remember that Feynman covered all of physics
  -- heavenly bodies through QED -- with only two levels of document hierarchy
  (_The Feynman Lectures on Physics_, 1970).

- The classical terminal manpage display is typographically well thought out.
  Big bold section headings, justified monospace text, nicely indented
  paragraphs, intelligently aligned definition lists, and an informational
  header and footer.

- Manpages have a simple referencing syntax; e.g., sh(1), fork(2), markdown(7).
  HTML versions can use this to generate links between pages.

Unfortunately, figuring out how to create a manpage is a fairly tedious process.
The roff/mandoc/mdoc macro languages are highly extensible, fractured between
multiple dialects, and include a bunch of device specific stuff irrelevant to
modern publishing tools.

## Features
  * Concise set of notes used for quick reference.
  * Git powered cheat sheet repository.
  * Custom sheets repo.
  * Fast!
  * Few dependencies (common now, you should have them (sed, git, etc))
  * Self updating via `cheat_fu -uself`
  * Instant cheat sheet updates via `cheat_fu -u`
  * Terminal cheats completion.

## Installing/Uninstalling

    $ git clone git://github.com/jpablobr/cheat_fu.git && cd cheat_fu
    $ sudo make install

Debian based distro:

    $ sudo dpkg --install ./cheat-fu_1.1-1_all.deb

Uninstall

    $ sudo make uninstall
    # Debian
    $ sudo dpkg --remove cheat-fu

Cheat_fu is just a bash shell script, therefore, you can just put it on one of your `bin` directories in your `$PATH` and you're ready to start cheating!

## cheat_fu help

`$ cheat_fu -h`

Will Output the help information.

    Options:
    -h, ,ch --help	Display this help message and exit.
    -s              Outputs a list of sheets matching [sheet] or all sheets
    -l              Outputs the path(s) to [sheet] or all sheets
    -u              Updates the cheat sheet repo to grab the latest changes.
    -u [self]       Updates cheat_fu.
    -v              Outputs current version.

    $ cheat_fu -r ronn

    Reads the exact <sheet> given. No globbing allowed here!

    $ cheat_fu -l ronn

    Output paths to sheets matching 'ronn'

    $ cheat_fu -s

    Output list of all sheets

    $ cheat_fu -u

    Update cheat sheet repository

    $ cheat_fu -u self

    Update the 'cheat_fu' executable

    Viewing sheet specifics
    cheat_fu ronn | grep :empty

## Making Roff Files:

`$ ronn --roff my_cheat.1.ronn`

This will output your Roff file.

`roff: ./my_cheat.1`

## Tips

   * Grep!, you would not have problems with things such as `$ cheat_fu ronn | grep :empty`
   * Aliases: `alias ct='cheat_fu'`
