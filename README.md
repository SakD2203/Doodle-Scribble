# Doodle-Scribble
<div align="center">
<h1>Doodle-Scribble</h1>
</div>

> A simple yet powerful canvas-drawing component for React ([Demo](https://github.com/SakD2203/Doodle-Scribble/))

[![Travis][build-badge]][build] [![Coveralls][coveralls-badge]][coveralls] [![npm package][npm-badge]][npm] [![downloads][downloads-badge]][npmtrends] [![MIT License][license-badge]][license]

[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors) [![PRs Welcome][prs-badge]][prs]

[![Watch on GitHub][github-watch-badge]][github-watch] [![Star on GitHub][github-star-badge]][github-star] [![Tweet][twitter-badge]][twitter]

## Installation

Install via NPM:

```
npm install react-canvas-draw --save
```

or YARN:

```
yarn add react-canvas-draw
```

## Usage

```javascript
import React from "react";
import ReactDOM from "react-dom";
import CanvasDraw from "Doodle-Scribble";

ReactDOM.render(<CanvasDraw />, document.getElementById("root"));
```

For more examples, like saving and loading a drawing ==> look into the [`/demo/src` folder](https://github.com/SakD2203/Doodle-Scribble/tree/master/Doodle-Scribble/demo/src).

### Props

These are the defaultProps of CanvasDraw. You can pass along any of these props to customize the CanvasDraw component. Examples of how to use the props are also shown in the [`/demo/src` folder](https://github.com/SakD2203/Doodle-Scribble/tree/master/Doodle-Scribble/demo/src).

```javascript
  static defaultProps = {
    onChange: null
    loadTimeOffset: 5,
    lazyRadius: 30,
    brushRadius: 12,
    brushColor: "#444",
    catenaryColor: "#0a0302",
    gridColor: "rgba(150,150,150,0.17)",
    hideGrid: false,
    canvasWidth: 400,
    canvasHeight: 400,
    disabled: false,
    imgSrc: "",
    saveData: null,
    immediateLoading: false,
    hideInterface: false
  };
```

### Functions

Useful functions that you can call, e.g. when having a reference to this component:

- `getSaveData()` returns the drawing's save-data as a stringified object
- `loadSaveData(saveData: String, immediate: Boolean)` loads a previously saved drawing using the saveData string, as well as an optional boolean flag to load it immediately, instead of live-drawing it.
- `clear()` clears the canvas completely
- `undo()` removes the latest change to the drawing. This includes everything drawn since the last MouseDown event.

