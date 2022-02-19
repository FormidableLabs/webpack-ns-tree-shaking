Webpack Namespace Experiments
=============================

This repo confirms that namespace imports are tree-shaken for at least the version of webpack used here.

So, an import like:

```js
import * as colors from "./colors/index.js";
```

Ends up being mostly equivalent, tree-shaking-wise, to:

```js
import { red } from "./colors/index.js";
const colors = { red };
```

To use try:

```sh
$ yarn build --mode production
```

and play around with `src/index.js`.


## Maintenance Status

**Archived:** This project is no longer maintained by Formidable. We are no longer responding to issues or pull requests unless they relate to security concerns. We encourage interested developers to fork this project and make it their own!
