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

* [default.hsfiles](templates/default.hsfiles)
  * a template for my personal project
  * hspec + doctest for testing
    * contains a sample file with sample haddock comments.
    * contains a sample spec file.
  * travis for CI
  * additional ghc options for warnings
  * my settings for hlint
* [with-standalone.hsfiles](templates/with-standalone.hsfiles)
  * basically same as the default but it contains a few additional items* which are:
    * Dockerfile
      * generates a docker image to run the output binary.
    * docker-build.sh
      * triggers docker build.
  * it requires your stack.yaml to have the following.

```yaml
docker:
  enable: false
  repo: utdemir/ghc-musl:v7-libgmp-ghc883
```
