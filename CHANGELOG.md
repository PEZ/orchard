# Changelog

## master (unreleased)

## 0.5.3 (2019-10-08)

### Bugs fixed

* [#74](https://github.com/clojure-emacs/orchard/pull/74): Don't check for internet connectivity for local ClojureDocs cache URLs.

## 0.5.2 (2019-10-02)

### Bugs fixed

* [#72](https://github.com/clojure-emacs/orchard/pull/72): Check for internet connectivity before downloading ClojureDocs exported file.

## 0.5.1 (2019-09-11)

### Bugs fixed

* [#69](https://github.com/clojure-emacs/orchard/pull/69): Include specs in `var-meta`.

## 0.5.0 (2019-08-29)

### New features

* [#42](https://github.com/clojure-emacs/orchard/pull/42): Add namespace alias support for `spec-list` and `spec-form`.
* [#46](https://github.com/clojure-emacs/orchard/pull/46): [Inspector] Separate static from non-static fields when rendering raw objects.
* [#46](https://github.com/clojure-emacs/orchard/pull/46): [Inspector] Show fields inherited from superclasses when rendering raw objects.
* [#47](https://github.com/clojure-emacs/orchard/pull/46): [Java] Cache class-info for editable Java classes.
* [#51](https://github.com/clojure-emacs/orchard/issues/51): Add basic xref functionality in `orchard.xref`.
* [#64](https://github.com/clojure-emacs/orchard/issues/64): Port `cache-dir` from [soc/directories-jvm](https://github.com/soc/directories-jvm) to `orchard.util.os`.
* [#64](https://github.com/clojure-emacs/orchard/issues/64): Add finding docs functionality from ClojureDocs in `orchard.clojuredocs`.
* Extract `cider-nrepl`'s resource lookup functionality into `orchard.java.resource`.

### Changes

* Update JavaDoc URL paths for Java 10+. Remove support for Java 7 JavaDoc URL paths.
* Remove dependency on `clojure.tools.namespace` (replaced by `orchard.namespace`).
* Remove dependency on `java.classpath` (replaced by `orchard.java.classpath`).
* Add java parser for JDK9+; rename legacy JDK8 parser.
* Make search for JDK directory resources compatible with JDK9+.
* Move `transform-value` to `cider-nrepl`.

### Bugs fixed

* [#59](https://github.com/clojure-emacs/orchard/pull/59): Correct inlined-dep prefix for removing namespaces
* [#57](https://github.com/clojure-emacs/orchard/pull/57): Fix parsing of Java versions for Java 11+.

## 0.4.0 (2019-01-14)

### New features

* [#38](https://github.com/clojure-emacs/orchard/pull/38): [Inspector] Add eval
  and def features to inspector.

### Bugs fixed

* [#39](https://github.com/clojure-emacs/orchard/pull/39): Catch `LinkageError` when calling `Class/forName`.

## 0.3.4 (2018-12-29)

### Changes

* [#35](https://github.com/clojure-emacs/orchard/pull/35): [Inspector] Render Java's lists, maps, and arrays as collections.
* [#35](https://github.com/clojure-emacs/orchard/pull/35): [Inspector] Truncate long inline values.
* Ensure all classpath entries have absolute paths.

## 0.3.3 (2018-10-20)

### Bugs fixed

* [#33](https://github.com/clojure-emacs/orchard/pull/33): Address a NPE in `class-info` when dealing with classes created via `reify`.

## 0.3.2 (2018-10-14)

### Bugs fixed

* Figure out the package of classes defined with `deftype` and `defrecord` on Java 8.

## 0.3.1 (2018-09-15)

### Bugs fixed

* [#28](https://github.com/clojure-emacs/orchard/pull/28): Fix inspector dropping items after nil value.

### 0.3.0 (2018-06-16)

### New features

* Extracted info and eldoc functionality from `cider-nrepl` into `orchard.info` and `orchard.eldoc`.

## 0.2.0 (2018-05-07)

### New features

* Added a generic API for querying namespaces and vars (`orchard.query`).

## 0.1.0 (2018-05-04)

### New features

* Initial extraction of nREPL-agnostic functionality from `cider-nrepl`.

### Changes

* [#24](https://github.com/clojure-emacs/orchard/pull/24): [Inspector] Separately clickable keys and values when inspecting maps.
* [#24](https://github.com/clojure-emacs/orchard/pull/24): [Inspector] Remember page numbers for each nesting level.
