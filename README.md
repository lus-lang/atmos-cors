# cors

Adds Cross-Origin Resource Sharing to `web` applications.

```lus nocheck
local web = require("https://atmosp.here/2.0/web.lus")
local cors = require("https://atmosp.here/2.0/cors.lus")

local app = web.app()
app:register(cors, { origin = { "https://lus.dev" } })
```

The package requires Lus 2.0. It declares no permissions. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `cors.lus`. Run `lus doc cors.lus` to print it.
