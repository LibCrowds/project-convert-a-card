# project-convertacard

This is the parent template for the Convert-a-Card projects seen on LibCrowds.

The project has five main files:

- project.json: a JSON file that describes the project.
- long_description.md: a Markdown file with a long description of the project.
- template.html: the view for every task.
- tutorial.html: a simple tutorial for the volunteers.


## Installation

It's advised that you make a fork of this repository for each language where a
Convert-a-Card project is to be used. Once that fork is created, and configured
as described below. You can use the PyBossa [pbs](https://github.com/PyBossa/pbs)
command line tool to create the projects.


## Configuration

There are a few things that will need to be configured for each language.


### Trusted institutions

The `libs` variable at the top of the JavaScript section of [template.html](template.html)
contains a list of trusted institutions. Only records created or modified by these
institutions will be returned in the WorldCat search results.


### Long description

Add a short paragraph to the bottom of [long_description.md](long_description.md) to say a
bit about that particular collection, for example:

```
## About the Pinyin Card Catalogue

This card catalogue covers about 40,000 printed items...
```

