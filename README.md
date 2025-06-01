# pluto-zip

A zip reader library for Pluto.

## Documentation

This library exports the following functions:
- `list(bin)`
- `read(bin, path)`
- `readex(bin, offset, compressed_size)`

Example usage:

```lua
local zip = require "zip"

local bin = io.contents("my.zip")
print(dumpvar(zip.list(bin)))
print(zip.read(bin, "my.txt"))
```
