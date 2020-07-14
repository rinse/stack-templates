# Haskell Stack Templates

## Table of contents
  1. [Table of contents](#table-of-contents)
  2. [How to use](#how-to-use)
  3. [Templates](#templates)

## How to use

* Use a template locally
  1. Place them in $HOME/.stack/templates
  2. `$ stack new {project name} {name of the template file}`

* Use a template on a remote server
  1. `$ stack new {project name} {url of the template file}`

## Templates

* [rinse.hsfiles](templates/rinse.hsfiles)
  * a template for my personal project
  * hspec + doctest for testing
    * contains a sample file with sample haddock comments.
    * contains a sample spec file.
  * travis for CI
  * additional ghc options for warnings
  * my settings for hlint
