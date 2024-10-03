# scsman
a suck/simple/stupid/shitty colorscheme manager aimed to be simple and minimal.
## install
just copy `scsman` to somewhere in `$PATH`
## usage
```
usage: scsman <option> <args>
option:
    help                             print this text.
    add <file> <name>                add <file> to the manager.
                                     will create a template named <name> at ./templates.
                                     omit <name> to use path as name instead.
    remove <name>                    if provided template name then remove the template.
                                     if provided file path then the template associated with that file will be remove.
                                     the manager will not manage the file associated with that template anymore.
    list <type>
        type:
            templates                list all template and their associated file,.
            colorschemes             list all colorschemes available.
    load <template> <colorscheme>    apply <colorscheme> to the file associated with <template>.
    load-all <colorscheme>           apply <colorscheme> to all the files added to manager.
```
- to add a colorscheme, copy a json file in `./example/colorschemes`, edit it then add it to `~/.config/scsman/colorschemes`. to use it just type in the file name without the extension.
### example
there are 2 colorschemes pre-written in `./example/colorschemes/` (`catppuccin-mocha` and `gruvbox`) and a `rofi` theme `./example/scsman.rasi`. make sure to copy `./example/colorschemes/` content to `~/.config/scsman/colorschemes/` before start.
- first copy `./example/scsman.rasi` into `rofi` config dir\
`cp ./example/scsman.rasi ~/.config/rofi/`
- next add the `rofi` config to scsman\
`scsman add ~/.config/rofi/scsman.rasi rofi`
- then replace all colors (for example #aabbcc) in `~/.config/scsman/templates/rofi` to `{<key>}`, here i just copy the pre-edited file into it\
`cp ./example/rofi.rasi ~/.config/scsman/templates/`
- now load the colorscheme\
`scsman load rofi gruvbox`
- finally config `rofi` to use the theme
## why not just use [wpgtk](https://github.com/deviantfero/wpgtk)?
- im lazy to learn new stuff
- wpgtk has a lot of stuffs that i dont need
- i just need a simple script for my [rice](https://github.com/mncc8337/awesomewm-dotfiles)
- i have nothing to do
- i want to try to implement this by myself
## inspiration
- [wpgtk](https://github.com/deviantfero/wpgtk) by deviantfero
