# javelin

## 2.4.0

*Sun Nov 24 12:34:02 EST 2013*

* add clojure implementation

## 2.3.0

*Wed Oct 30 16:09:26 EDT 2013*

* add `cell-map` function and `cell-doseq` macro

## 2.2.1

*Mon Oct 21 23:33:21 EDT 2013*

* add `make-require` and `make-require-macros`

## 2.2.0

*Mon Oct 21 16:41:17 EDT 2013*

* add `refer-all` macro

## 2.1.1

*Sun Oct 20 16:25:35 EDT 2013*

* rollback unquote fix in 2.0.3

## 2.1.0

*Sun Oct 20 14:22:48 EDT 2013*

* Feature: add `alts!` macro

## 2.0.3

*Sat Oct 19 18:24:43 EDT 2013*

* Bugfix: issue with syntax-unquoted references to cells in formulas

## 2.0.2

*Thu Oct 17 15:12:29 EDT 2013*

* Update dependencies to versions compatible with new CLJS version.

## 2.0.1

*Thu Oct 17 02:31:41 EDT 2013*

* Bugfix: issue with arg destructuring in anon fns in formulas

## 2.0.0

*Wed Oct 16 12:23:32 EDT 2013*

## 2.0.0-SNAPSHOT

*Wed Oct 16 11:12:01 EDT 2013*

* Use hoisting instead of lifting when constructing formulas.
* Unsupported special forms are now down to just `ns`, `def`, `deftype*`,
  and `defrecord*`.
* It is no longer an error to destroy a cell that other cells reference
  in their formulas.

*Mon Oct 14 14:08:09 EDT 2013*

* Add `defc` and `defc=` macros.

*Sun Oct 13 18:24:15 EDT 2013*

* Remove `mx` macro.
* Add `macroexpand-all` macro.
* Unsupported special forms in formulas now cause compile-time exception.
* Fix issue where local bindings were interpreted as special forms with the
  same name.
* The `cell?` function returns the cell or nil instead of boolean.
* Add `input?` macro.
* Watches can be added to input and formula cells. IWatchable is now fully
  supported again by all Cells.
* Move `tailrecursion.javelin.macros` namespace to `tailrecursion.javelin`.
* Remove `cell?`, `input?`, `cell`, `set-cell!`, and `destroy-cell!`
  macros&mdash;use the functions with corresponding names instead.

*Tue Oct  8 19:28:37 EDT 2013*

* Add `cell?`, `set-cell!`, `set-cell!=`, and `destroy-cell!` macros.

*Sun Oct  6 16:32:01 EDT 2013*

* Throw exception when `swap!` or `reset!` is applied to a formula cell.
* Watches can no longer be added to formula cells. Use cells instead.
* Remove macros `cfn` and `defcfn` from public API.
* Remove convenience functions `route*`, `timer*`, `log`, `timeout`, and
  `interval` from public API.
* Remove `self?` from public API and self-referential code.
* The `cell` macro creates only input cells; `cell=` creates only formula
  cells.
* Changes in the way macro builds formulas:
  * Quoted expressions are not walked but remain quoted.
  * The `unquote` form is repurposed: argument is evaluated in place and not
    walked.
  * The `unquote-splicing` form is interpreted as the composition of `unquote`
    and `deref`.

*Mon Sep 30 15:22:11 EDT 2013*

* Remove `done` property from `Cell` type.
* Remove `done!` from public API.
