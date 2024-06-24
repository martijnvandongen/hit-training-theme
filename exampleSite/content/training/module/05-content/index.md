---
title: "Content"
---

## Folder Structure

The folder structure is structured like a bookshelf. So every training is a **book**, each book contains several **modules** and each module contains several **chapters**. 

The prefix 10 of `10-module` and `10-chapter` are important. Usually in Hugo you configure a "weight" in the frontmatter, but I didn't like that. Pages in this theme are ordered based on foldername. This ensures the order shown in the website is the same as your source code structure. For books that's not important.

```text
└── content
    ├── _index.html
    └── book
        ├── _index.md               // 1
        └── 10-module
            ├── _index.md           // 1
            ├── 10-chapter1         // 2
            │   ├── img
            │   │   └── photo.png 
            │   └── index.md 
            ├── 20-chapter1
            │   └── index.md
            ├── 30-chapter3
            │   └── index.md
            └── 99-appendix
                ├── _index.md
                └── slidedecks     
                    ├── part-1.md   // 3
                    ├── part-1.md   // 3
                    └── _index.md   // 3
```

1. `content/book/_index.md` and `content/book/10-module/_index.md` must be present, but only contains a title to show in the web pages. You never navigate to this page unless you explicitly type the url: /book or /book/10-module. These pages respectivily show a list of modules or a list of chapters.
2. It's recommended to put all pages in folders. Hugo supports pages as files, but that could be confusional for image folders.
3. The appendix 