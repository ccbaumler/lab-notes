# lab-notes
A simple, easy lab notebook website

> - Note: Consider integrating your HackMD or Obsidian with your GitHub account. This ***could*** make formatting each of your markdown files a simpler task. Check out [Issue #1](https://github.com/ccbaumler/lab-notes-template/issues/1) for more detailed information.

## Intended usage

To automatically update a simple website with your markdown documents!

That's it.... Thanks?

## Set up

To create your own website!

1. Fork this repo as `lab-notes`
   > When forking you have the option of renaming the fork. Rename your fork to remove `_templates` from its name for a simpler URL.
3. Click `Settings` > `Pages`
4. In the `Source` dropdown, select `Deploy from a branch`
5. In the `Branch` dropdown, select `main` then click `Save`
6. There is now a `Your site is live at` followed by a URL!
   > Note: You may need to refresh the page.
7. Head back to `<> Code`, in the upper right hand corner there is an `About` section
   1. Click the `Settings` (Actually looks like this -> ⚙️)
   2. Toggle the checkbox under `Website` that says `Use your GitHub Pages website`
8. Update the title yaml header in the `index.md` file with your name
   i. Something like `<YourName>'s Lab Notebook` (e.g. `Brenda's Lab Notebook`)

## How to use

The idea was a straight-forward one when I thought this up. Each markdown document added to the `docs` directory will become a link on your website. Each link will take you to the rendered markdown document on a new nested website. The trick was to automate this! (For those interested in Github Actions as an automation tool, check out the [.github/workflows/update_index.yaml](https://github.com/ccbaumler/lab-notes-template/blob/main/.github/workflows/update_index.yaml) file!)

1. Consider removing the `notes-template.md` file in the `docs` directory... or don't and just keep it and update it in to a template that works for you.
2. Add any number of your own **markdown** documents to the `docs` directory
   - **The document file name must not contain any whitespaces and must end in `.md`**
   	   - Whitespaces in filename will not work! (eg. `whitespaces in file names.md`)
   	   - Filename must contain `.md` at the end! (eg. `must-contain-.-md-at-the-end`)
     - Name the files similar to this -> `2024-week-1.md`.
3. The contents of the document will be [rendered as markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
4. If you want to have unique titles for each document, include a yaml header with `title:`. See the template below.

## A basic document template for you (specifically)

```
---
title: Year Week number
---

# Goals
In this section I will list the weekly, quarterly, and yearly goals I hope to achieve or have completed this week.

**Weekly:**
- [x]  Create a lab notebook repo
- [ ]  Read the docs

**Quarterly:**
- [ ] Present my work to the lab
- [ ] Write some python code
- [ ] Write some snakemake files

**Yearly:**
- [ ] Have a well documented project in github that is functional (if not perfect)

# Results
In this section write the verbatim results (eg. copy the code chunks, error reports, plots) that relate to the goals you have achieved this week.

example:
This week I created a lab notebook repo using this method (include the cli arguments and the process below)

# Discussion
In this section explain your results and how they relate to you goals

example:
I am applying for credit this quarter. Therefore, I chose to create a lab notebook repo in github to continue practicing git and github as it is an important tool for biotech/bioinformatics.

# Journal
In this section add anything else you may wish to include.

example:
Nothing additional to comment this week. Work has been taken allot of my time this week. It's finals, I was not able to complete the goals I thought I would. I got a new hamster and it is very fluffy.
```

## Resources (ie. The things I looked at to avoid other work and how I figured out how to do this!)

1. [github actions commit bot](https://github.com/orgs/community/discussions/26560#discussioncomment-3531273)
2. [github markdown syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
3. [github jekyll themes](https://pages.github.com/themes/)
4. [github theme title fix](https://github.com/pages-themes/cayman/issues/134#issuecomment-1000227220)
5. [easy markdown to github pages](https://nicolas-van.github.io/easy-markdown-to-github-pages/)
