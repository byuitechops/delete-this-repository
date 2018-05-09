# Fix Relative Path
### *Package Name*: fix-relative-path
### *Child Type*: post import
### *Platform*: all
### *Required*: Recommended

This child module is built to be used by the Brigham Young University - Idaho D2L to Canvas Conversion Tool. It utilizes the standard `module.exports => (course, stepCallback)` signature and uses the Conversion Tool's standard logging functions. You can view extended documentation [Here](https://github.com/byuitechops/d2l-to-canvas-conversion-tool/tree/master/documentation).

## Purpose

People sometimes put in relative paths to file in Canvas (i.e. `/course_files/aFolders/theFileName.docs`) but that means that moving the file breaks the link. The child module needs to switch out relative path link to links that use the item ID instead.

## How to Install

```
npm install fix-relative-path
```

## Run Requirements

None 

## Options

None

## Outputs

None

## Process

1. Get all Module Item HTML
2. Find all `<a></a>` tags that don't have a domain or `http://`
3. Find where the link is supposed to lead to
4. Change out the `href=""` in the `<a></a>` tags that have the relative links
5. PUT the changes to canvas 

## Log Categories

- Links Updated

## Requirements

Swap out all relative links with literal links.