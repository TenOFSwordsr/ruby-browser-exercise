# sample_Browser - Unimplemented Ruby Web-Browser Exercise

A two-file Ruby skeleton for a command-line web browser: a `Browser` REPL class and a `Page` model
to fetch and parse a URL with Nokogiri. Nothing is implemented - every method body is a comment
describing what should go there, and the file ends with two open questions about quitting and asking
for help. It is a course-style starting point, left unfinished.

**Suggested repo name:** `ruby-browser-exercise`
**Stack:** Ruby, `net/http`, `nokogiri`
**Status:** experimental
**Last modified:** 2019-12-04

## What it does

As written, it establishes the intended shape and nothing more:

- `sample_Browser/browser.rb` - `Browser#run!` carries comments only: run a prompt, read user input,
  instantiate a `Page` and call methods on it. The file then calls `Browser.new.run!` at load time,
  so executing it does nothing and returns immediately.
- `sample_Browser/page.rb` - `Page#initialize(url)`, `fetch!`, `title` and `links` are empty stubs.
  The `links` comment states the requirement: extract only absolute URLs of the form
  `<a href="http://somesite.com/page.html">`.
- `browser.rb` does `require_relative 'util'`, and no `util.rb` exists in the folder, so loading it
  as-is raises a `LoadError` before any of it runs.

## Layout

```
sample_Browser/browser.rb   REPL shell, comments only, instantiates Page
sample_Browser/page.rb      fetch / title / links stubs
```

## Notes

- Not functional, and there is no README-worthy behaviour to document - the value is the requirement
  comments if you want to finish it later.
- The folder sits under a `Py` tree but contains only Ruby. The extension and the parent directory
  name disagree with the contents.
- `page.rb` never requires `net/http` or `nokogiri` even though the stubs imply it would need them;
  those requires live only in `browser.rb`.
