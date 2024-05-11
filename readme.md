# scsman
a suck/simple/stupid/shitty colorscheme manager i wrote aimed to be simple and minimal.
## usage
- add a file to be managed: `./scsman add <file> <name>`
- replace colors (#aabbcc) in the file `templates/<name>` to `{<key>}`, with \<key\> being any keys in `colorschemes/*.json` (`color0` to `color15`, `active` and `inactive`)
- `./scsman load <name> <colorscheme>` to load colorscheme\
`./scsman load-all <colorscheme>` to load all\
\<colorscheme\> is the json file name (with out extension) in `./colorschemes/`\
see `scsman help` for more options
### example
there are 2 colorschemes pre-written in `./colorschemes/` (`catppuccin-mocha` and `gruvbox`) and a `rofi` theme `./examples/scsman.rasi`
- first copy the theme into `rofi` config dir\
`cp ./examples/scsman.rasi ~/.config/rofi/scsman.rasi`
- next add the `rofi` config to scsman\
`./scsman add ~/.config/rofi/scsman.rasi rofi`
- then replace all colors (#aabbcc) in `templates/rofi` to `{<key>}`, here i just copy the pre-edited file into it\
`cp ./examples/rofi ./templates/rofi`
- now load the colorscheme\
`./scsman load rofi gruvbox`
- finally config `rofi` to use the theme
## why not just use [wpgtk](https://github.com/deviantfero/wpgtk)?
- im lazy to learn new stuff
- wpgtk has a lot of stuffs that i dont need
- i just need a simple script for my [rice](https://github.com/mncc8337/awesomewm-dotfiles)
- i have nothing to do
- i want to try to implement this by myself
## inspirations
- [wpgtk](https://github.com/deviantfero/wpgtk) by deviantfero
