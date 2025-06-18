# Snippets for EASIFEM

This repository contains the snippets for fortran code in EASIFEM. It also contains the markdown snippets for writing documentation of EASIFEM.

The fortran snippets are contained in `fortran.json` file and the markdown snippets are contained in `markdown.json` file.

You can use these snippets in your code editor.

## Using snippets in neovim

Clone this repository by using one of the ways given below:

HTTPS:

```bash 
https://github.com/easifem/snippets.git
```

SSH:

```bash
git@github.com:easifem/snippets.git
```

GitHub CLI:

```bash
gh repo clone easifem/snippets
```

Step-2: Move these snippets to `neovim` config folder. 

```bash 
mkdir -p ~/.config/nvim/snippets
cd snippets
cp fortran.json ~/.config/nvim/snippets/easifem-fortran.json
cp markdown.json ~/.config/nvim/snippets/easifem-markdown.json
```

Step-3: Add config files to `package.json`

```bash 
cd ~/.config/nvim/snippets/
```

Open the `package.json` file and add the following.

```bash
{
  "name": "vscode-like-nvim-snippets",
  "author": "Sharma, Vikas",
  "engines": {
    "vscode": "^1.11.0"
  },
  "contributes": {
    "snippets": [
      {
        "language": ["markdown"],
        "path": "easifem-markdown.json"
      },
      {
        "language": ["fortran", "markdown"],
        "path": "easifem-fortran.json"
      }
    ]
  }
}
```

