inspirations:

- The Minimal Manual
    https://swcarpentry.github.io/swc-releases/2017.02/instructor-training/files/papers/carroll-minimal-manual-1987.pdf
- Literate Programming
    http://www.literateprogramming.com/knuthweb.pdf
- APL:  An Interactive Approach
    http://www.softwarepreservation.org/projects/apl/Books/GillmanAndRose

https://www.springer.com/gp/authors-editors/book-authors-editors/your-publication-journey/manuscript-preparation

Write like SeeTee shareholder letter but for Urbit, demolish all objections

https://www.coindesk.com/how-to-build-an-internet-where-communities-thrive

https://github.com/fmarotta/kaobook

https://third-bit.com/2021/01/27/essence-of-teaching/

- set up chapter author footnote and endnotes so each chapter stands alone

https://github.com/Fang-/Urbit-By-Doing/blob/master/talkbot/4.md


```c
' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~';
```

Runes within families are presented in the order that they occur in ASCII.  This ordering applies to all runes except `++ford` runes, which are presented in the order they are parsed.  Runes are furthermore presented as either _fundamental_ or _sugar_ runes, based on whether they are syntactic calques of other runes.  Relatively importance is indicated by division into _major_ and _minor_ runes.  Digraphs (such as `::` colcol "comment") are also indicated in their naturally ordered positions.  Some obsolete runes are included in case one encounters out-of-date Hoon code.

```
!#$%&*+-.:;<=>?@^_|~
```

For every major rune we introduce, we present at least three working examples with as much context as deemed necessary.  For each minor rune, we include at least one example of complete use and one instance of use in the kernel.

Each rune (except for `!!` zapzap "crash") accepts at least one child.

## `|` Bars (Cores)

### `|$` barbuc (minor)

`|$ (lest term) spec`
produces a mold

grep -r "|\\$" | wc -l
37

### `|%` barcen (major)

`|% (unit term) (map term tome)`
produces a core (battery and payload)

grep -r "|%" | wc -l
872

### `|*` bartar (major)

`|* [spec value]`
produces a wet gate (a one-armed core with sample)

grep -r "|\\*" | wc -l
385

### `|-` barhep (major)

`|- hoon`
produces a trap (a core with one arm) and evaluates it

grep -r "|-" | wc -l
716

### `|.` bardot (medium)

`|. hoon`
produces a trap (a core with one arm)

grep -r "|\\." | wc -l
268

### `|:` barcol (minor)

`|: [hoon hoon]`
produces a gate with a custom sample

grep -r "|\\:" | wc -l
31

### `|=` bartis (major)

`|= [spec value]`
produces a dry gate (a one-armed core with sample)

### `|?` barwut (minor)

`|? hoon`
produces a lead trap

grep -r "|?" | wc -l
4

### `|@` barpat (minor)

`|@ (unit term) (map term tome)`
produces a wet core (battery and payload)

grep -r "|@" | wc -l
37

### `|^` barket (medium)

`|^ hoon (map term tome)`
produces a core whose battery includes a $ arm and computes the latter

grep -r "|^" | wc -l
229

### `|_` barcab (major)

`|_ spec alas (map term tome)`
produces a door (a core with sample)

grep -r "|_" | wc -l
289

### `|~` barsig (minor)

`|~ [spec value]`
produces an iron gate

grep -r "|~" | wc -l
89
