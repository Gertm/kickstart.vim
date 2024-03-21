# kickstart.vim

![kickstart-vim-screenshot](./kickstart-vim-screenshot.jpg)

### Introduction

Kickstart.vim is a Vimscript version of [Kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim).
Like Kickstart.nvim, Kickstart.vim strives to be:

> A starting point for ~~Neovim~~ Vim that is:
>
> * Small
> * Single-file ~~(with examples of moving to multi-file)~~
> * Documented
> * Modular

### Installation

> [!NOTE]
> I highly recommend you to [fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo so that you can manage your own configuration

Option #1: Manually copying and pasting the contents of the `.vimrc`

**Option #2: Creating a symbolic link**

This is an easy way to manage your Vimrc with Git as well as other configuration files.

0. Backup your existing `.vimrc` (e.g., `mv ~/.vimrc ~/.old-vimrc.bak`)
1. clone the repository in your home directory
    ```bash
    git clone https://github.com/Gertm/kickstart.vim.git ~/src/kickstart.vim
    ```
2. Create a symbolic link between `~/src/kickstart.vim/.vimrc` and `~/.vimrc`
    ```bash
    ln -sf ~/src/kickstart.vim/.vimrc ~/.vimrc
    ```
3. Now whenever you open `~/.vimrc`, you are opening `~/kickstart.vim/.vimrc`.
    Since `kickstart.vim` is a Git repository, you can easily manage changes you made to your `.vimrc` across multiple devices.

### Post Installation

Run the following command and launch Vim again, and you are ready to go!

```bash
vim +PlugInstall +qa
```

### Changes from Kickstart.nvim

kickstart.vim:

- is written in Vimscript (:surprised Pikachu face:) and designed for Vim >= 0.8
- uses Vim alternative for the following plugins
    - [lazy.nvim](https://github.com/folke/lazy.nvim) -> [vim-plug](https://github.com/junegunn/vim-plug)
    - [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig) and other LSP plugins -> [vim-lsp](https://github.com/prabirshrestha/vim-lsp)
    - [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) -> [supertab](https://github.com/ervandew/supertab)
    - [which-key.nvim](https://github.com/folke/which-key.nvim) -> [vim-which-key](https://github.com/liuchengxu/vim-which-key)
    - [gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim) -> [vim-gitgutter](https://github.com/airblade/vim-gitgutter)
    - [onedark.nvim](https://github.com/navarasu/onedark.nvim) -> [onedark.vim](https://github.com/joshdick/onedark.vim)
    - [lualine.nvim](https://github.com/nvim-lualine/lualine.nvim) -> [vim-airline](https://github.com/vim-airline/vim-airline)
    - [indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim) -> [indentLine](https://github.com/Yggdroot/indentLine)
    - [Comment.nvim](https://github.com/numToStr/Comment.nvim) -> [vim-commentary](https://github.com/tpope/vim-commentary)
    - [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) -> [fzf](https://github.com/junegunn/fzf) & [fzf.vim](https://github.com/junegunn/fzf.vim)
- **enables some settings enabled by default in Neovim (e.g., filetype, syntax, autoindent, etc.)** on the top of kickstart.nvim settings
- enables `hlsearch`
- disables `undofile` by default, but the instructions for changing `undodir` and enabling `undofile` are included
- does not provide an alternative for:
    - highlight on yank
    - **nvim-treesitter**

