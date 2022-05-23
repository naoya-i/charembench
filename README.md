# Character Embedding Benchmark

## What is this?

This dataset aims for testing the quality of representations of characters in novels.
The benchmark dataset probes what kind of character-related information, ranging from gender to authors, is embedded in character embeddings.
It consists of 12 different tasks categorized into three levels: (i) characterlevel tasks: identifying character attributes, (ii) context-level tasks: identifying the correct character that best describes a given context, and (iii) book-level tasks: identifying the attributes of books where characters come from.

See the following paper for further details:

Naoya Inoue, Charuta Pethe, Allen Kim, Steven Skiena. Learning and Evaluating Character Representations in Novels. Findings of the Association for Computational Linguistics: ACL 2022. https://aclanthology.org/2022.findings-acl.81/


## Dataset

All files are JSON-formatted. Here is the list of tasks and their corresponding JSON files:

- Character-level task
    - Gender: `data/char_level/gender.js`
    - Role: `data/char_level/role.js`
    - Protagonist: `data/char_level/protago.js`
    - Identity: `data/char_level/ident.js`
- Context-level task
    - Cloze: `data/ctx_level/cloze.js`
    - Speaker: `data/ctx_level/speaker.js`
    - QA: `data/ctx_level/qa.js`
- Book-level task
    - Author: `data/book_level/author.js`
    - Book: `data/book_level/book.js`
    - Genre: `data/book_level/genre.js`

In each file, characters are represented by `(Project Gutenberg Book ID)_(Character ID)` (e.g. 113_0).
You can obtain full texts of original books from the Project Gutenberg website by using this ID, e.g., https://www.gutenberg.org/ebooks/113.
You can find mappings from character ID to character names in `data/chr_map.json`.


## Notes
- As described in the paper, the QA task is extracted from https://github.com/deepmind/narrativeqa.
- The datasets for Desc and SummaryCloze are not here because of copyright issues.
