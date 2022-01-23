# plenv-install-blead

This is a [plenv](https://github.com/tokuhirom/plenv) plugin,
that helps you install perl from the perl source repository https://github.com/Perl/perl5

# Install this plugin

```console
git clone https://github.com/skaji/plenv-install-blead $(plenv root)/plugins/plenv-install-blead
```

# Usage

First you need to clone https://github.com/Perl/perl5 into a local direcotory,
and set the directory to `PLENV_INSTALL_BLEAD_REPOSITORY`:

```console
git clone https://github.com/Perl/perl5 $HOME/.perl-source
export PLENV_INSTALL_BLEAD_REPOSITORY=$HOME/.perl-source
```

Then:

```console
❯ plenv install-blead HEAD
---> git clone -q --reference /Users/skaji/src/github.com/Perl/perl5 https://github.com/Perl/perl5 /Users/skaji/env/plenv/build/blead-20220123-133537
---> git -C /Users/skaji/env/plenv/build/blead-20220123-133537 checkout -q HEAD
---> Using prefix /Users/skaji/env/plenv/versions/blead-v5.35.8-7-g8030c9e253
---> Configure/build/install perl, see /Users/skaji/env/plenv/build/blead-20220123-133537.log
---> ./Configure -des -Dman1dir=none -Dman3dir=none -Dusedevel -Uversiononly -Dprefix=/Users/skaji/env/plenv/versions/blead-v5.35.8-7-g8030c9e253 -Dscriptdir=/Users/skaji/env/plenv/versions/blead-v5.35.8-7-g8030c9e253/bin
---> make -j8 install
---> Successfully install perl into /Users/skaji/env/plenv/versions/blead-v5.35.8-7-g8030c9e253
---> You may want to execute: plenv global blead-v5.35.8-7-g8030c9e253

❯ plenv global blead-v5.35.8-7-g8030c9e253

❯ perl -v
This is perl 5, version 35, subversion 9 (v5.35.9 (v5.35.8-7-g8030c9e253)) built for darwin-2level
```

Try `plenv install-blead --help` for the more detailed explanation.

# Author

Shoichi Kaji

# License

Apache License 2.0
