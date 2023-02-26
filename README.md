# basic_cookie
The simplest toy example possible for a [cookiecutter](https://cookiecutter.readthedocs.io/en/stable/) project, used for teaching

`cookiecutter` is a python library for creating your own project or repository templates.

The key components to note:

## The `cookiecutter.json` file

* `cookiecutter.json` : Here you specify which variables to prompt the user that will feed into your project template. Each key in the key-value pair indicates a variable that can be used in the template and each value specifies a default value. 

```json
{
    "project_name": "sample_project",
    "greeting": "Hello, World!"
}
```

## `{{this notation}}` means something will be filled in later

The double bracket `{{...}}` notation is a feature of Jinja notation - you can insert it anywhere in your template repo and it'll be replaced by the variable specified in the `cookeicutter.json` file.

For instance, the project directory is `{{ cookiecutter.project_name }}`, so on project creation it will query the user for a `project_name` or use the default`project_name` value specified in the `cookiecutter.json` file. 

## Use the cookiecutter

To use the template, in the console just `cookiecuttter` the url of this git repo, i.e.:

```console
cookiecutter https://github.com/banditkings/basic_cookie/
```
