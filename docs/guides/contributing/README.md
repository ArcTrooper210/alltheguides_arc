---
title: Contributing to ATG
description: How to contribute!
authors:
 - ArcTrooper
 - Seg
nav:
 - examples
---

# All The Guides [![](https://img.shields.io/github/actions/workflow/status/AllTheMods/alltheguides/mkdocs.yml?style=flat-square&label=mkdocs)](https://github.com/AllTheMods/alltheguides/actions/workflows/mkdocs.yml) [![](https://img.shields.io/github/actions/workflow/status/AllTheMods/alltheguides/publish.yml?style=flat-square&label=publish)](https://github.com/AllTheMods/alltheguides/actions/workflows/publish.yml)

![GitHub Repo stars](https://img.shields.io/github/stars/AllTheMods/alltheguides?style=flat-square) ![GitHub forks](https://img.shields.io/github/forks/AllTheMods/alltheguides) ![GitHub watchers](https://img.shields.io/github/watchers/AllTheMods/alltheguides?style=flat-square) ![GitHub](https://img.shields.io/github/license/AllTheMods/alltheguides?style=flat-square)

---

## **Setup Not Required!**

You do not ***have*** to setup mkdocs for ATG! This guide is mainly for those that plan to make multiple contributions to ATG or want to preview the formatting for their guide.

If you want to make a one time contribution or don't want to go through all the trouble of setting up mkdocs, you can always write up your guide in a text file and send it to @ArcTrooper or one of the mods on [Discord!](https://discord.com/invite/allthemods)

---

## Guidelines

???+ Information "MUST READ"

    !!! Warning "As this guide is currently work-in-progress, guidelines are expected to change."

    1. You may **NOT** publicly republish **All The Guides** live on another website.
    2. You may **NOT** delete or entirely change another author work (except typos / incorrect information), unless given permission to do so from the original **Author**. 
    3. No warnings or errors that prevents `uv run mkdocs serve | build`.
        1. If you get any errors or warnings, try/get help resolving them before pushing. 
        2. You may **NOT** disable `strict` mode(s) for any reason.
    4. Your document(s) **MUST** contain a `title` and `description` variable. If you created a page, you may add `authors:`, and additional variables if necessary. [Read Below](#document-headers)
    5. Limit or prevent the use of outside links to content (documents or imagery). If possible in the most minimal and or compressed way, include the content with your document.
        1. This would ensure that content will always remain with the guides, for preservation and offline use.
        2. Assets may be included with document(s) within folders in an organized way.
    6. No profanity, and assets and or links to outside websites that contains adult like content, paid material, and or in-appropriate things.
        1. You'll be **banned** from future **PR's**.
    7. You shall **NOT** touch `mkdocs.yml`, `pyproject.toml`, or workflow files, _unless authorized, and you know what you're doing_.
    8. Documentation should ONLY be related to **All The Mods**, if it needs to be.
    9. Javascript is **NOT** allowed.
    10. Folders & files must be in `lowercase` letters, with no spaces. `Camelcase` for image files is allowed.
---

**All The Guides** uses [Github Pages](https://pages.github.com/), [MkDocs](https://www.mkdocs.org/) & [Material](https://squidfunk.github.io/mkdocs-material/).

---

## Local Serve / Build 

We use **Github** for our Packs, Mods, and Guides for Collaboration, and CI/CD purposes.

You will be required to [Serve](#serve), and [Build](#build) this guide, which comes with some minimal [Requirements](#requirements). 

---

### Requirements

- [Python](https://www.python.org/downloads/) 3+
- Git ([Github Desktop](https://desktop.github.com/) or [Git Cli](https://cli.github.com/))
    - _Your editor may already have Git integrated_
    - For quick edits, you could open a codespace on your forked repo using [Github Web Editor](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor).
- [UV Package Manager](https://docs.astral.sh/uv/getting-started/installation/#winget)
    - We recommend the `winget` installation method, if you're on Windows.

> You are **not** required to have knowledge of them (_specifically **Python**_), but they must be installed..

---

## Setup

Fork [All The Guides](https://github.com/AllTheMods/alltheguides/fork).

### Clone / Checkout `mkdocs` branch

The __`mkdocs`__ branch is the live - up to date branch that should be used _primarily_. This should be selected by default when you clone the repo.

Depending on current setup, you may have an editor (_Visual Studio Code_), that has **Git** integration. You're free to use this, Github Desktop or Git.

---

#### GitHub Desktop

Go to `File` -> `Clone repository...` OR do `Ctrl+Shift+O` and select your All the Guides fork.

!!! info "I recommend putting the repository under `C:/Users/yourPCName` for easy access"

---

#### Git CLI

``` title="Change 'USERNAME' to your GitHub name"
git clone https://github.com/USERNAME/alltheguides
```

---

### Enable Workflows

???+ danger "Make sure Workflows are enabled, otherwise PR's will **NOT** be accepted."
    ![](img/workflow.png)

---

### Install UV and Python Dependencies

Install **UV**

```
winget install --id=astral-sh.uv  -e
```

All The Guides requires some Python dependencies that are used to [build](#build) and provide features for the Guide itself.

```
uv sync
```

---

## Serve

Serve will launch a server locally to test changes live @ [`localhost:8000`](http://localhost:8000). Importantly, it will provide warnings, errors, and {~~ mistakes (_spelling errors_) ~> disabled for the time being, use Grammarly or another spellchecker ~~}. Once changes are satisfied without issues, test your [Build](#build) before you commit / make a Pull Request.

```
uv run mkdocs serve
```

---

## Build

Build will finalize compiling **Markdown** and output **HTML** files in the `site` folder. This folder should be _ignored_. The build should succeed ***without*** any warnings or errors before [Committing](#commit-updating) and submitting a [Pull Request](#pull-request).

```
uv run mkdocs build
```

---

## Commit (Updating)

Once you're _committed_ to your changes, you can then **Commit** your changes, then make a **Pull Request** against both `mkdocs` branches / repositories.

### Committing Changes

Depending on current setup, you may have an editor (_Visual Studio Code_), that has **Git** integration. You're free to use this, Github Desktop, or Git.

???+ information "Making a GitHub commit with GitHub Desktop"
	All changes made will be selected by default, if you do not want to commit some changes, deselect those.
	
	Fill out the `Summary` and `Description` on the bottom left, click `Commit to mkdocs` when you're ready to commit.
	
	If you made a mistake, you can undo the commit in the bottom left. Otherwise click `Push origin` to push the commit to GitHub.

??? Information "Making a Github commit with Git"
    Add files to Commit.
    ```
    git commit .
    ```

    Add a message to your Commit. We recommend being more descriptive about your Commit(s).
    ```
    git commit -m "update"
    ```

    Push changes
    ```
    git push
    ```

---

## Pull Request

When submitting a [Pull Request](https://github.com/AllTheMods/alltheguides/compare), you're requesting us to **Pull** changes from your Repository (Fork) to be approve & merged into the official Guide. This is done in browser by going to our repository and creating a [Pull Request](https://github.com/AllTheMods/alltheguides/compare) from your `mkdocs` branch to ours.

---

## Making a Document

!!! Warning "Before we begin, make sure you've read the [Guidelines](#guidelines)."

Documents must be Markdown (`.md`) files. They can also contain **HTML**. 

This Guide is a mix of [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), [Material](https://squidfunk.github.io/mkdocs-material/reference/), and [PyMarkdown](https://python-markdown.github.io/) features. Simply placing a `.md` file within `docs/`, that file can then be viewed as a page. **Note**: `.md` files MUST contain content.

Markdown files should have headers at the start to identify document (_Meta / SEO Purposes_), and to credit author(s). Without, it's subjected to be generated based off page content, or be without at all.

---

### Document Headers

???+ danger "Warning"
	Do **NOT** use ++tab++ to indent a list of authors in the `authors` section of document headers. It *WILL* cause errors.

!!! Warning ""

    !!! Note ""

        Highlighted lines are required!!

```yaml title='example.md' hl_lines="2 3 10"
---
title: Title of Your Document
description: Description of your doc
authors: 
 - John Doe
 - Second Name
 - Florida Man
---

# mainPageHeader

Content.

## someTitle

Content.

> modName | [modName](legacy CurseForge link)

```

???+ Information "Descriptions"

	- `title:`
		- The page title of your document
	- `description:`
		- The description of your page/what it's about. Only shows in the embed of links
	- `authors:`
		- The list of authors that have contributed to this document.
	- `comments:`
		- Enable/Disable the use of comments on your page. Default: `false`

!!! warning "Your page should start with a `H1` (`#`) page header!"

---

### Configure Pages and Navigation (Optional)

???+ danger "Warning"
	Do **NOT** use ++tab++ to indent new lines in `.pages` files. It *WILL* cause errors.

Per directory, you can create a `.pages` file. This can be used to list each and all pages you want to show up on navigation, in your own order.

```yaml

nav:
  - page1
  - page2.md

  - dir/
  - dir/README.md

  # Can change page titles
  - "3 Is better" : page3.md

  # Navigation link to another website
  - "Google" : https://google.com

  # custom sub navigation
  - 'MORE PAGES':
    - page1
    - page2

  - page1
    - page2
    - page3
  
  # 3 dots will auto generate the rest of the pages you've not defined from current directory
  # THIS IS REQUIRED IF YOU'RE MAKING A NAV FILE.
  - ...
```

---

### Directory / Page Layout

This is the directory layout that **MkDocs** uses.

- **`docs`** | Main folder **MkDocs** will build site contents
    - **`cats`** | Custom site directory that can be accessed from **`/cats/`**
        - **`.pages`** | Optionally can be used to organize sidebar pages/hierarchy.
        - **`README.md`** | Root directory file that **should** be in each folder.
        - **`food.md`** | A page that can be accessed from **`/cats/food`**
    - **`.pages`** | Optionally can be used to organize sidebar pages/hierarchy.
    - **`README.md`** | Root directory file that **should** be in each folder.
    - **`name.md`** | Your unique page name.

`README.md`
: Is the root directory file, if no page is visited specifically.

---

### More Resources

> Most of all necessary plugins are installed and can be used from Material / PyMarkdown, however consult the team for any additions.

- [Examples of most of all Markdown features](examples/README.md)
- [Writing Your Docs](https://www.mkdocs.org/user-guide/writing-your-docs/)
- [Material MarkDown](https://squidfunk.github.io/mkdocs-material/reference/)
- [PyMarkdown Extension](https://python-markdown.github.io/extensions/)

---

## FAQ

??? question "My header is displaying above the page title!"
	- It usually means that you put a `Tab` indent somewhere. Likely in your list of authors.
	
	![](img/faqHeader.png){style='border: 1px solid orange'}

??? question "My author's list is spelling them out letter by letter!"
	- You didn't put a space after the dash. `- authorName` not `-authorName`
	
	![](img/faqAuthor1.png){style='border: 1px solid orange'}
	
??? question "My locally hosted preview won't refresh with changes!"
	- Check your PowerShell console output and read any warnings it spits out. It will tell you exactly what files are causing the error.
	- It is likely a misspelled file name or you have the incorrect path to an image.
	
	![](img/faqWarning.png){style='border: 1px solid orange'}


> All The Mods | [GitHub](https://github.com/AllTheMods) | [Discord](https://discord.com/invite/allthemods) | [Akliz Server Hosting](https://www.akliz.net/allthemods)
