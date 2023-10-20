# Best Practices guidelines

This document contains a set of guidelines that should be followed when developing a new feature or fixing a bug in the Python web application project. These guidelines are not strict rules, but they are a good starting point to ensure that the code is consistent and easy to read. If you have any questions, feel free to ask them in the [Issues](https://github.com/Style77/Style77/issues) section.

#### Motivation

I ran in to an issue while writing test cases for my CRUD application. I was unsure if I should write test cases for the `partial_update` and `update` views, since they are very similar and how many more tests should I write. I decided to write this document to help me and other developers to write better code. Every section were strictly researched and tested, so you can be sure that the information is correct.

## Table of Contents

>!Table of contents for now will contain only few actually finished sections, but it will be constantly updated in the future.

- [Best Practices guidelines](#best-practices-guidelines)
      - [Motivation](#motivation)
  - [Table of Contents](#table-of-contents)
  - [General](#general)
    - [Naming](#naming)
    - [Comments](#comments)
  - [Django REST Framework](#django-rest-framework)
    - [Naming](#naming-2)
    - [Comments](#comments-2)
    - [Imports](#imports-2)
    - [Code formatting](#code-formatting-2)
    - [Code structure](#code-structure-2)
    - [Code style](#code-style-2)
    - [Tests](#tests)
  - [Git](#git)
    - [Naming](#naming-4)
    - [Comments](#comments-4)
    - [Imports](#imports-4)
    - [Code formatting](#code-formatting-4)
    - [Code structure](#code-structure-4)
    - [Code style](#code-style-4)
  - [Resources](#resources)

## General

### Naming

Most of the naming conventions are taken from [PEP 8](https://www.python.org/dev/peps/pep-0008/).

- Use `snake_case` for variable, function and method names.
- Use `PascalCase` for class names.
- Use `UPPER_SNAKE_CASE` for constants.
- Use `lowercase` for module names.
- Use `lowercase` for file names.
- Use `lowercase` for URL names, if it's related to endpoints use `lowercase`, `plural` - if it's not meant to be nested and always add slash `/` at the end of the URL.
- Use `lowercase` and `plural` for database names.
- Use `lowercase` and `plural` for model names.
- Use `lowercase` and `plural` for serializer names if they are meant to be used as a list, otherwise use `lowercase` and `singular`.
- Use `lowercase` and `singular` for viewset names. However if the viewset is nested, use `lowercase` and `singular` for the parent viewset and `lowercase` and `plural` for the child viewset e.g. `workspace/{id}/keys/`.
- Use related model name, endpoint method and type of object + word `Test`, for test case names e.g. `WorkspaceUpdateViewTest`.

### Comments

Comments are basically useless, you should never use them if they doesn't contain any special information like `todo`, `fixme` or when you copy code from another source like `stackoverflow`, so other developers will be able to understand problem you ran in to that made you copy code to fix it. If you need to use comments, you should refactor your code to be more readable.
