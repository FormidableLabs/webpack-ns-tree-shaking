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
