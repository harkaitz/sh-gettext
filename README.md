# SH-GETTEXT

## Help

gettext-h-i18n

    Usage: gettext-h-i18n ...
    
    Internationalize (i18n) a software project using "xgettext".
    
      -V        : List available settings (put them in .gettext).
      -l        : List source code.
      -u        : Update ".po" files with new texts.
      -b        : Build the ".mo" files.
      -g go|... : Generate utility code, ie "i18n.go".
    
    Examples:
    
      $ gettext-h-i18n -ubg go

gettext-h-i18n--go

    Usage: gettext-h-i18n--go GO...
    
    Print textx between l("TEXT") in go files. You must define
    manually `func l(s string) string { return s }` function in
    internationalizable packages.

gettext-h-i18n--go-gen

    Usage: gettext-h-i18n--go-gen
    
    Create "i18n.go" file with definitions for l() and newError[E,S]().

gettext-h-i18n--html

    Usage: gettext-h-i18n--html HTML...
    
    Print texts between {{.T "TEXT"}} in html files.

gettext-h-i18n--toc

    Usage: gettext-h-i18n--toc < FILE-LIST
    
    For each input file create a FILE.i18n file with it's texts
    in C format _("TEXT"); This way xgettext(1) can be used with
    unsupported programs.

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
