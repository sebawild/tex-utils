# tex-utils
A collection of LaTeX utilitities I ended up using in many projects.
The main idea of each is to keep simple things simple (if you are not willing to peek at `sty` files, this might not be
the right repo for you).
Emphasis is on easy maintainability, compatibility and adaptability, with a reasonable (not not the most convenient possible) 
interface.  
Cars don't have a sealed hood with no way to patch things up; software shouldn't either.


## wref

Simple non-clever (a feature!) package for `\ref`erences that include their type, e.g., `\wref{sec:intro}` translates to “Section 1”, 
and the full phrase becomes a clickable pdf link (not only the number).
Selection of the type prefix is done by label name (instead of trying any error-prone automatic mechanism to guess it
from the aux file).

This package was born out of frustration with semi-smart packages like cleveref, and I find it much more maintainable
and extendable.


## notestoself

Add notes to your paper and decide how they are inserted:

 * as inline todo-notes,
 * as margin notes revealed/hidden on click (using advanced pdf layer feature called optional content groups (OCGs)),
 * collected at the end of the document.
 
 My main motivation for creating this was to support (almost) arbitrary tex in the notes, not only text or otherwise
 restricted formats. (Some glitches remain, but most won't stop compilation)

 
## url-doi-arxiv

Little hacks to get consistent formats (using `\urlfont` for doi, urls, and arxiv links (e.g. in bibliographies).
Borrows code from existing packages, but adds hooks to change styles.


## placed-saved-box

Two simple versatile commands intended for `beamer` presentations: 

* `\\placedbox` allows to put some content at an absolute position on the page, above other content. Very useful for popups and visual hacks on slides.
* `\\savedbox` allows to use complicated content including beamer overlay specifications inside other things where those would break because they are typeset several times. It works by first storing the content in a savebox. This is used inside placedbox.


## wclrscode

A modified version of clrscode3e with a few pseudocode syntax tweaks:

* assignment (`\gets`) uses `:=` instead of `=`
* equality (`\isequal`) check uses `==` instead of `=`
* less spacing around codeboxes (for use in floats)
* Comments use sans-serif font
* smaller line numbers
* added for each, end for, end if, end while keywords
