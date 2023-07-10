### There are three commits:

You might need to force `npm i -f`

#### Chart works without components:
* Here the gantt chart is just a regular svelte component and index.js exports it.
* public/index.html directly imports the bundle.js into its body.
* The chart works in the html component

#### Button does work as component:
* Shows that a regular button inside a svelte component works.
* The index.html uses the button as a regular html element (gantt chart isn't exported here, so nvm)

#### Gantt chart is messed up:
* Instead of the button I export the Gantt chart component, which looks all messed up
