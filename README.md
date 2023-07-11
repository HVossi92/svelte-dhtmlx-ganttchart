## Problem
How to create a working web component (to use in AngularJs) from a svelte component using the DHTMLX Gantt Chart library?

### Fixed
Fixed with the last commit. Update to Svelte 4 and disable shadow dom in the component.
The public/index.html uses the svelte component and works stand alone, with the rest of the build files.

### There are three commits describing the problem:

#### Chart works without components:
* Here the gantt chart is just a regular svelte component and index.js exports it.
* public/index.html directly imports the bundle.js into its body.
* The chart works in the html component

#### Button does work as component:
* Shows that a regular button inside a svelte component works.
* The index.html uses the button as a regular html element (gantt chart isn't exported here, so nvm)

#### Gantt chart is messed up:
* Instead of the button I export the Gantt chart component, which looks all messed up

You might need to force `npm i -f`