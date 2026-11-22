# cors

`cors` adds Cross-Origin Resource Sharing to `web` applications. It answers preflight requests and adds the `Access-Control-*` headers to the responses of the origins that a program allows.

The following example accepts cross-origin requests from `https://lus.dev` only.

```lus nocheck
local web = require("https://atmosp.here/2.0/web.lus")
local cors = require("https://atmosp.here/2.0/cors.lus")

local app = web.app()
app:register(cors, { origin = { "https://lus.dev" } })
```

The package requires Lus 2.0 and declares no permissions. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `cors.lus`, which `lus doc cors.lus` prints.
