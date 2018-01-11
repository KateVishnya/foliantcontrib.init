# Project initializer for Foliant

This CLI extension add `init` command that lets you create Foliant projects from templates.


## Installation

```shell
$ pip install foliantcontrib.init
```


## Usage

Create project from the default “basic” template:

```shell
$ foliant init
Enter the project name: Awesome Docs
✔ Generating Foliant project
─────────────────────
Project "Awesome Docs" created in /path/to/awesome-docs
```

Create project from a custom template:

```shell
$ foliant init --template /path/to/custom/template
Enter the project name: Awesome Customized Docs
✔ Generating Foliant project
─────────────────────
Project "Awesome Customized Docs" created in /path/to/awesome-customized-docs
```

You can provide the project name without user prompt:

```shell
$ foliant init --name Awesome Docs
✔ Generating Foliant project
─────────────────────
Project "Awesome Docs" created in /path/to/awesome-docs
```

Another useful option is `--quiet`, which hides all output except for the path to the generated project:

```shell
$ foliant init --name Awesome Docs --quiet
/path/to/awesome-docs
```

To see all available options, run `foliant init --help`:

```shell
$ foliant init --help
usage: foliant init [-h] [-n NAME] [-t NAME or PATH] [-q]

Generate new Foliant project.

optional arguments:
  -h, --help            show this help message and exit
  -n NAME, --name NAME  Name of the Foliant project
  -t NAME or PATH, --template NAME or PATH
                        Name of a built-in project template or path to custom one
  -q, --quiet           Hide all output accept for the result. Useful for piping.
```


## Project Templates

A project template is a regular Foliant project, but with `title` value in `foliant.yml` replaced with the `{title}` placeholder. When the project is generated, the placeholder is replaced with the actual project name.

There is a built-in template called "basic." It's used by default if you don' specify the template.

>   **Note**
>
>   More placeholders and built-in templates may be added in future versions.
