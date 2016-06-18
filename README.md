# `grab-mac-link.el`

Grab link from Mac Apps.

## Supported Apps

- Chrome
- Safari
- Firefox
- Finder
- Mail
- Terminal

## Supported Link types

    Plain:    https://www.wikipedia.org/
    Markdown: [Wikipedia](https://www.wikipedia.org/)
    Org:      [[https://www.wikipedia.org/][Wikipedia]]


## Usage

### `M-x grab-mac-link`

Prompt for an application to grab a link from and prompt for a link
type to insert as, then insert it at point.

### `(grab-mac-link app &optional link-type)`

Grab link from App and return it in LINK-TYPE.

``` emacs-lisp
(grab-mac-link 'chrome)
    ⇒ "https://www.wikipedia.org/"

(grab-mac-link 'chrome 'plain)
    ⇒ "https://www.wikipedia.org/"

(grab-mac-link 'chrome 'markdown)
    ⇒ "[Wikipedia](https://www.wikipedia.org/)"

(grab-mac-link 'chrome 'org)
    ⇒ "[[https://www.wikipedia.org/][Wikipedia]]"

(grab-mac-link 'terminal)
    ⇒ "/Users/xcy/.emacs.d"
```

## Acknowledgment

AppleScript code used in this program is borrowed from [`org-mac-link.el`](http://orgmode.org/worg/org-contrib/org-mac-link.html).
