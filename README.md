# Comment TS
"Comment TS" generates a template for JSDoc comments. It is adapted for TypeScript files. Typescript comes with a lot of language annotations, which should not be duplicated in the comments. Most likely this would lead to inconsistencies.

Avoids warnings like:
* warning TS0: @static annotations are redundant with TypeScript equivalents
* warning TS0: @private annotations are redundant with TypeScript equivalents
* warning TS0: the type annotation on @param is redundant with its TypeScript type, remove the {...} part

Optionally additional TODOs are autogenerated.

## Tags
Supported JSDoc tags: @description, @param, @returns, @template.

## Conventions
* Let method/function names start with a verb.
* Use camelcase

## Commands
### To add a comment
* press `Ctrl+Alt+C` twice
* or select 'Comment code' from your context menu
* or insert /** above the line of code.

Generates comments for whatever the caret is on or inside of.

The comments will look like:
```
  /**
   * documents this
   * @param editor
   * @param commandName
   * @param forCompletion
   * @returns
   */

  /**
   * Creates an instance of Documenter.
   */

  /**
  * Checks spelling
  * @param str
  * @returns true if spelling
  */

  /**
  * Capitalizes first letter
  * @param str
  * @returns
  */
```
### To update an existing comment
If some parameters have changed, you might want to preserve comments of unchanged parameter.
* Select the comment block you want to update and
* press `Ctrl+Alt+C` twice
* or select 'Comment code' from your context menu
* or insert /** above the line of code.

## Settings
* "comment-ts.todoComments": If true a // TODO: line is added to the comments. If you are using an extension like [todo tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree) you will find all comment TODOs in an explorer view.
* "comment-ts.replaceComments": Selected JSDoc comment will be updated. If parameters are added/deleted, comments of remaining parameters won't get lost.
* "comment-ts.includeDescriptionTag": Adds @description before your comment.
* "comment-ts.includeAuthorTag": Adds an @author tag to your comment.
* "comment-ts.authorName": The text behind the @author tag.
* "comment-ts.parseNames": Parses the names so as to generate comments. E.g. GetAccessor will produce "Gets <name> ". SetAccessor will produce "Sets <name> ", method camelcase names will be split, verbs get an s, except in special cases,...

## Documentation generator
* [Compodoc](https://compodoc.github.io/website/)
  Generate your Angular project documentation in seconds.

* [TypeDoc](http://typedoc.org/guides/installation/)
A documentation generator for TypeScript projects.

## The original codebase is from Document This. Thanks to the contributors!
