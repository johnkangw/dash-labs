# Overview
Unlike other Plotly projects, `dash-labs` does **not** adhere to semantic versioning. This project is intended to make it easier to discuss and iterate on new ideas before they are incorporated into Dash itself. As such, maintaining backward compatibility within the `dash-labs` package is explicitly a non-goal.

## 1.0.0

### Added
 - Added Dash Pages: A plug-in to simplify building multi-page apps.
 - Added documentation: 08-MultiPageDashApp.md and 09-MultiPageDashAppExamples.md.
 - Added demos:  examples of multi-page apps using the Dash Pages plug-in.

### Removed
 - removed code, tests, and demos for projects documented in chapter 02 through 07.

## Changes
 - updated documentation to include status of projects in chapters 02 through 07.

## 0.4.0

### Added
 - Added Windows support for the `@app.long_callback` decorator ([#32](https://github.com/plotly/dash-labs/pull/32))
 - Added caching support to the `@app.long_callback` decorator using the `cache_by` argument ([#32](https://github.com/plotly/dash-labs/pull/32))
 - Add support for updating arbitrary component properties while a long_callback is running using the `set_progress` function. 

### Changes
 - To enable Windows support, the FlaskCaching backend to `@app.long_callback` has been replaced by a backend based on the `daskcache` library


## 0.3.0

### Added
 - Added Dash app plugins to support a new `@app.long_callback` decorator to support long-running callback functions ([#24](https://github.com/plotly/dash-labs/pull/24)).

### Changes
 - Replace use of "role" with "location" throughout the templates API ([#25](https://github.com/plotly/dash-labs/pull/25)).
 - Remove `_input`/`_output` suffix from template component builders, and replace with `new_` prefix ([#25](https://github.com/plotly/dash-labs/pull/25)). 


## 0.2.0

### Changes
 - Replaced `tpl.layout(app)` method with `tpl.children` property ([#20](https://github.com/plotly/dash-labs/pull/20))

### Documentation
 - Added documentation chapter with additional examples of template usage


## 0.1.0

This is the initial release of `dash-labs` which includes:
 - The `dash_labs.plugins.FlexibleCallbacks` plugin which enables advanced `@app.callback` functionality like property grouping and the ability to provide components in place of component ids.
 - A new template system that aims to make it easier to quickly create a variety of simple, nice looking, Dash apps with less code.
 - A new component plugin system that makes it possible to bundle components and callback functionality into composable classes. Several demonstration component plugins are included as well.
