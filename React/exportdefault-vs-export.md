### Difference between export default and export in React.js

#### export default (Default Export)
* a module can have only one default export
* when importing a default export, you can use any name (no need to match the exported name)

#### export (Named Export)
* You name the export when exporting the function, component, or variable
* A module can have multiple name exports
* When importing, you need to use the same name as the exported member (or use 'as' to alias it)

#### When to use each in React:
* Use export default when your module only exports one main component
* Use named exports when the module contains multiple components or utilities from the same file
