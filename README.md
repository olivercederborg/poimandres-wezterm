# Poimandres for Wezterm

## Screenshots

Base                       |  Storm
:-------------------------:|:-------------------------:
![Poimandres Base](https://user-images.githubusercontent.com/47901349/179416018-ba8e24a6-3590-4eff-93cb-806d41378a0d.png)  |  ![Poimandres Storm](https://user-images.githubusercontent.com/47901349/179416088-89677f33-ef8a-4e2d-87e8-e9a2c93e9832.png)

## Installation

Currently you can only apply this colour scheme with the Lua version, which includes a `setup` function to change the flavour of the theme.

**The steps**: 

1. Clone this repo, or download the [poimandres.lua](https://github.com/olivercederborg/poimandres-wezterm/blob/main/poimandres.lua) file.

2. **If you're on a POSIX system**: create a `colors` directory in your wezterm config path, e.g. `~/.config/wezterm/colors`. **If you're on Windows**: create a `colors` directory in the same directory as `wezterm.exe`, e.g. `C:\Program Files\WezTerm`. *If you're unsure of the config location for your system, take a look at the [WezTerm documentation](https://wezfurlong.org/wezterm/config/files.html)*

3. Move `poimandres.lua` to the `colors` directory created in step 2.

4. Add the following to your main WezTerm config file, e.g. `~/.config/wezterm/wezterm.lua`.

```lua
local wezterm = require('wezterm')
local poimandres = require('colors/poimandres').setup {}

return {
  colors = poimandres,

  -- rest of your config
}
```

5. *Optionally* change the flavour in the setup function.

```lua
local poimandres = require("colors/poimandres").setup {
  flavour = 'storm' -- default: 'base'
}
```

6. That's it!

## Related

- [poimandres.nvim](https://github.com/olivercederborg/poimandres.nvim): Neovim version
- [poimandres-theme](https://github.com/drcmda/poimandres-theme): VSCode version
- [poimandres-alacritty](https://github.com/z0al/poimandres-alacritty): Alacritty version
- [poimandres-iterm](https://github.com/alii/poimandres-iterm): Iterm version

### Hyper theme

```bash
hyper i hyper-pmndrs
```
