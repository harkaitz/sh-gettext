# NAME

gettext-h-i18n - An interface to "xgettext" for program internationalization

# SYNOPSIS

    vi GetText
    gettext-h-i18n -ub

# DESCRIPTION

This program helps internationalizing (i18n) a software project using
the "xgettext" utilities.

# STEP1 - Write the configuration file

The first step is to create a `.gettext`, `GetText` or `gettext` file
and to set the following variables there.

    GETTEXT_H_FIND_CMD='find . -iname "*.c"'
    # The command to use for listing internationalizable text files.
    
    GETTEXT_H_LANGS='en es ...'
    # The languages for which you want to create localized texts.
    
    GETTEXT_H_DOMAIN='package-name'
    # A package name to identify your program. It can be anything.

You can check the variables are set correctly executing:

    $ gettext-h-i18n -l : List sources using GETTEXT_H_FIND_CMD
    $ gettext-h-i18n -V : Show configuration variables.

# STEP2 - Add boilerplace file.

Some programming languages require some boilerplate in your project
to be internationalizable. You can execute a generator to create add
this code to the project.

Generators are named as "geni18n_LANG". For example in a go project:

    $ gen18n_go # Will create "i18n.go".

# STEP3 - Check programming language support.

Each programming language uses a different message extraction mechanism.

The extractors are scripts named as "extract-messages_LANG". Example:

    $ gettext-h-i18n -L
    html   extract-messages_html
    go     extract-messages_go
    
    $ extract-messages_go hello.go
    Hello World

# STEP4 - Update the po files and mo files.

Each time you edit the code, execute "gettext-h-i18n -u" to update
the message database.

    $ gettext-h-i18n -u
    locale/es/hello.po: 1 translations missing.
    locale/en/hello.po: 1 translations missing.

Edit the po files. Then update the final mo files.

    $ gettext-h-i18n -b

# STEP4 - Localization (l10n)

Once all messages are internationalized (i18n) your program needs to
peek the correct messages depending of the user preferences. This
libraries are supported:

    go: github.com/harkaitz/go-gettext-l10n

# COLLABORATING

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
# SEE ALSO

**XGETTEXT(1)**
