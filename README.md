# tex-utils
A collection of LaTeX utilitities I ended up using in many projects.
The main idea of each is to keep simple things simple (if you are not willing to peek at `sty` files, this might not be
the right repo for you).
Emphasis is on easy maintainability, compatibility and adaptability, with a reasonable (not not the most convenient possible) 
interface.


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
 * as foldable margin notes (using advanced pdf layer features),
 * collected at the end of the document.
 
 My main motivation for creating this was to support (almost) arbitrary tex in the notes, not only text or otherwise
 restricted formats. (Some glitches remain, but most won't stop compilation)
 
 ## url-doi-arxiv
 Little hacks to get consistent formats (using `\urlfont` for doi, urls, and arxiv links (e.g. in bibliographies).
 Borrows code from existing packages, but adds hooks to change styles.
