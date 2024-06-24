---
title: "Getting Started"
menus:
    main: {}
---

## Introduction

This theme is designed to build courses and publish them online. 

Features to highlight:

* Clean & calm user interface, responsive and mobile friendly (try the browser zoom!)
* All content, pages and slides, are written in markdown
* Pages and slides contain beautiful code blocks with highlighting
* Anyone can edit the content, if you're a little bit tech savvy
* Re-usable diagrams & images in your slides
* Slides can quickly be editted to your needs, just seconds before you start
* Diagrams (in svg) are much sharper and draw.io is integrated in VSCode to easily update images

## Technologies used

I'm using quite a lot of free and open source tools in this theme. All content is written in markdown. Markdown is a markup language that automatically generates headings, bold text, code blocks with highlighting, tables, etc.

* **Hugo**. Hugo is a static website generator, which is enriched with a couple of plugins called shortcodes.
* **Bootstrap**. Bootstrap is a beautiful open source front end framework, so the website looks pretty on your computer, tablet and phone.
* **RevealJS**. RevealJS is a html-presentation tool. It turns markdown into beautiful slides. 
* **Draw.io**. With draw.io you can create nice diagrams. Save the file as "filename.drawio.svg" and you can view it in SVG formatted images. Sharp images, easy to update in VSCode with a plugin.
* **VSCode**. VSCode is my preferred IDE. It's free and works like a charm for tools like this.

## Compare to other systems

Why are other learning themes not good enough? For example: Hugo learning theme, Doctave, Docusaurus. First of all, they are awesome! I tried them all. They are beautiful, easy to use, flexible, etc. Few reasons why I built this platform:

* It's even easier to use, almost no configuration required.
* It has revealjs slides integrated.
* Designed for "courses" and "learning", not for "documentation".
* Less bugs (I experienced with for example Hugo Learning Theme).

## Content Organization

Folder structure is the same, if you have only one course, a few or many.

* Content
    * Training1
        * Module1
            * Chapter1
            * Chapter2
    * Pages
        * RandomPage1
        * RandomPage2

### 1-5 courses on this website

* Keep the course name simple, for example: "Math", "English", "History".

Open the first module of a file `01-math/01-beginners/01-introduction/index.md` file and add:

```text []
---
title: "Introduction" # Chapter Name, not Training Name!
menus:
    main:
        title: "Math"    # Training Name, not Chapter Name!
        weight: 10
---
```

### 5-10 courses or courses with long names

If there are long names, make a submenu:

Open the first chapter index.md file and add:

```text []
---
title: "Introduction"
menus:
    main:
        title: "Math for data scientists"
        weight: 10
        parent: "Courses"
---
```

### 15+ courses, probably even more

Categorize your courses. For example:

* Languages
    * Dutch
    * English
    * French
* Programming
    * Python
    * Go
    * Java

```text []
---
title: "Getting Started"      # Chapter 1 in Module 1 in Course Name
menus:
    main:
        title: "Python"       # Course Name
        weight: 10
        parent: "Programming" # Keep short names
---
```