# FullCalendar React bundled as UMD

The goal was to bundle @fullcalendar/react in a single file with some plugins:

* @fullcalendar/interaction
* @fullcalendar/daygrid
* @fullcalendar/timegrid

And to have the `FullCalendar` component, and each plugin readily available
in `js` namespace once imported as a foreign library in a ClojureScript project.

react and react-dom are not included in the bundle and must be provided
somehow as peer dependencies (reagent 9.0.1 or higher in our case).

The CSS for the [standard theme](https://fullcalendar.io/docs/themeSystem)
is included in the JS bundle.

## Installation

```bash
yarn install
```

## Build Commands

```bash
yarn build # builds files into dist/ directory
yarn clean # start fresh
```

Derived from:
https://github.com/fullcalendar/fullcalendar-example-projects/tree/master/react

You can consider this as a hack to import a foreign lib.
[Cleaner](https://clojurescript.org/guides/webpack)
[approaches](https://gist.github.com/jmlsf/f41b46c43a31224f46a41b361356f04d)
exist to work with npm dependencies in ClojureScript.
