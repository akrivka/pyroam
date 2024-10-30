> [!WARNING]
> This plugin is currently unmaintained!

# 🐍 pyroam - Python notebooks in Roam Research

`pyroam` lets you execute python code inside [Roam Research](https://roamresearch.com/) using [pyodide](https://github.com/pyodide/pyodide). Now you can do [literate programming](https://en.wikipedia.org/wiki/Literate_programming)!

![pyroam gif](/docs/assets/pyroam.gif)

Showcase video:
(Watch on [Loom](https://www.loom.com/share/3148a7aa34144795ace5bc69c2859267?sid=4d634cb6-d8e4-4aa4-be4c-047361a25acf)

https://github.com/user-attachments/assets/a7c3d21e-c9b4-4126-9ee3-6cd3f1706f2f


## Usage

The main thing you need to know are the two following keybindings:

| Keybinding         | Action           |
| ------------------ | ---------------- |
| <Alt+Enter>        | Run current cell and write |
| <Alt+Shift+Enter>  | Run all cells in *active notebook* and write |

When a codeblock is run, the output is written to the block nested one below it. 

The fastest way to add a Python codeblock in Roam is by typing `/python` and pressing Enter.

### Active notebooks

By default, the current page is the *active notebook*, i.e., when you press <Alt+Shift+Enter>, all blocks on the current page get run and their outputs are written. 

You can designate a smaller portion of the page to be the *active notebook* by referencing the page `[[pyroam/notebook]]` in the parent block, i.e. all blocks nested under this blocks will get run when pressing <Alt+Shift+Enter>, but no other. You can also nest notebooks - the plugin will always run the "smallest" one. 

All variables are shared, it's like if the code blocks were one script.

### Packages

Currently, `numpy`, `matplotlib` and `scipy` get loaded, though `numpy` tends to be buggy and plot generation with `matplotlib` doesn't work yet. 

In the future, the plugin will load all imported packages dynamically (as long as `pyodide`, the underlying Python browser compiler, allows it). 


## Bug reports & Contributing
You can create issues or pull requests in the [repository](https://github.com/aidam38/pyroam) or DM me on Twitter (https://twitter.com/adam_krivka)
