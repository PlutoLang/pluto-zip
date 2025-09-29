# pluto-zip

A zip library for Pluto.

## Documentation

This library exports the following functions:
- `list(bin)`
- `read(bin, path)`
- `readex(bin, offset, compressed_size, uncompressed_size)`
- `create(files)` — note that no compression will be performed

### Example: Creating a zip

```lua
local zip = require "zip"

io.contents("hello.zip", zip.create({
    ["hello.txt"] = "Hello from pluto-zip!"
}))
```

### Example: Reading a zip

```lua
local zip = require "zip"

local bin = io.contents("hello.zip")
print(dumpvar(zip.list(bin)))
print(zip.read(bin, "hello.txt"))
```
