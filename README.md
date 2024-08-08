
# NVL Library: nvl.async

This library is part of the NVL project and is currently in early development.
Please note that it is a work in progress.

## Design Notes

My first idea was to inject the name `vim` into the globals table `_G` and provide
corresponding functions when not running in the `Neovim` process. This would
however tie the functions to the `Neovim` API directly and create an unnecessary
dependency which is not needed when working on a plain Lua project.

I found it better and easier to read when you declare the imports at the top level
of your Lua file.

```lua
local async = require("nvl.async")
local schedule = async.utils.schedule -- uses vim.schedule or an equivalent 
```

## Scope

The NVL Library offers a collection of commonly used functions and classes designed for Lua and Neovim runtimes.

### Sources

- `neovim/runtime/lua/shared.lua`: Contains all functions that can be utilized in any Lua runtime environment.

## Credits

Special thanks to the following teams and developers:

- Neovim Team
- tjdevries: Author of `plenary.nvim` and `telescope.nvim`

Feel free to reach out for further information or if you encounter any issues.
