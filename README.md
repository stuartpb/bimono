# Bimono

This repository contains experiments in developing a monosyllabic "language" of under 1024 words, using the hexadecimal consonants `BDFGHJKLMNPRSTVZ` and quaternary vowels `AIOU` laid out in [A Proposal for Proquints][proquint], and (initially) the thousand most common words in the English language as defined and used by Randall Munroe's [Thing Explainer][TE].

[proquint]: https://arxiv.org/html/0901.4016
[TE]: https://xkcd.com/thing-explainer/

## Phases

phase1.txt describes the most straightforward encoding: all words are sorted alphabetically, and encoded based on their position in the list.

This ordering, however, presents some problems: for instance, the first word in the list, the indefinite article "a", is mapped to the word "BAD", meaning that the phrase "a good word" is translated to "BAD JOB ZIK", the phrase "a bad job" is translated to "BAD BUZ KUH", and "the best haircut" is translated to "TIS DIN JOZ GAR".

phase2.txt describes an ongoing effort to rearrange the words as defined in Phase 1 to be in closer approximation to their pronunciation, or some other form of mnemonic (eg. "two", "with", and "bite" are moved to "DOS", "MIT", and "NOM", respectively). Under Phase 2's reckoning, "a good word" is "DAH GUD VOD", "a bad job" is "DAH BAD JOB", and "the best haircut" is "DUH BOS FUR KUT".

## Roadmap

Phase 3 of this project might work toward making it so that the concepts described by the monosyllabic words are linguistically-neutral concepts, rather than retaining the English-specific pitfalls of the first two phases:

- Homographs and homonyms (such as "lead" and "mine") are conflated together.
- Many synonyms (such as "boat" and "ship") are redundant to each other (Randall himself notes that he eschews "ship" for "boat" in Thing Explainer).
- Some words (such as "bedroom") are redundant with combinations of shorter words (such as "bed" and "room").

Phase 4 and onward might look toward addressing how this word list focuses on lemmas (like "explain"), without a way to denote derivations such as "-er" (as in "explainer"). Future phases may also consider a more semantic sorting of concepts, rather than trying to fit words around existing ethnographic pronunciations.

## Copyright

Whether or not these word lists constitute copyright infringement is something
of an [open question][legal], legally speaking: I haven't contacted Randall Munroe
about this project yet, so I don't feel that I can safely declare a license for this project.

[legal]: https://opensource.stackexchange.com/questions/10670/copyrightablity-of-word-lists
