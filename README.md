# JavaScript/TypeScript Development Environment

> My presentation notes and resources for establishing a competent JS/TS
> development environment aimed at new programmers

**Goal**: Introduce relatively new developers interested in JavaScript and
TypeScript to ways that they can optimize their development workflows.

One of the best investments a programmer can make is in their own development
environment. Successful programmers are constantly tweaking and tuning their
development environment to **work for them**. Saving 5 seconds on a task
executed 50 times daily, like code formatting, could save you ~18 hours/year.
Multiply this times the number of automations you can find in your development
workflow and you can find yourself literally saving months of effort.

**TL;DR**: If you're a programmer, **invest in yourself**.

Much of this series is centered around VSCode and its extensions, but the
concepts can generally be applied to other text editors. I've personally used a
similar stack in VIM/Neovim previously as well as IntelliJ — it's generally a
matter of translating the configuration and finding the right plugins.

Generally, I tend to program on macOS and the demos in this series will take
place on macOS virtual machine, everything in this series works cross-platform.

## `whoami`

I'm a Lead Developer (Full-stack) at a large company you've hopefully heard of
with ~20 years of experience programming, with an emphasis on front- and
back-end web development. I spend a significant amount of time tuning my
development environment to work for me, and hope sharing some of what I've
learned provides value to others.

## Prerequisites

- [Volta](https://volta.sh)
  - Pinning Node.js + npm/Yarn
  - Installing global tools

## Code Quality

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  - Configure to validate all JS/TS files
    ```json
    "eslint.validate": [
      "javascript",
      "javascriptreact",
      "typescript",
      "typescriptreact"
      // also can add "svelte" or "vue" here too
    ],
    ```
  - Install
    [eslint-config-standard](https://github.com/standard/eslint-config-standard)
  - Install
    [eslint-config-standard-with-typescript](https://github.com/standard/eslint-config-standard-with-typescript)
  - Install
    [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- Configure VSCode to "Format On Save"
  ```json
  "[javascript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint",
    "editor.formatOnSave": true
  },
  ```

## Productivity

- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
- [Document This](https://marketplace.visualstudio.com/items?itemName=oouo-diogo-perdigao.docthis)
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

## Visual Enhancements

- [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.material-theme)
  - Disable Markdown styling: `"oneDarkPro.markdownStyle": false,`
- [VSCode Great Icons](https://marketplace.visualstudio.com/items?itemName=emmanuelbeziat.vscode-great-icons)
- [Fira Code Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)
  - `"editor.fontFamily": "'FiraCode Nerd Font', Menlo, Monaco, 'Courier New', monospace",`
  - `"editor.fontLigatures": true,`
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [Github Markdown Preview](https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview)
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
- [TODO Tree](https://marketplace.visualstudio.com/items?itemName=gruntfuggly.todo-tree)

## VSCode Settings

- `"editor.renderWhitespace": "all",`
- `"editor.rulers": [80],`
- Right-aligned workbench
  - `"workbench.panel.defaultLocation": "right",`
  - `"workbench.sideBar.location": "right",`

## Extras

- [VSCode Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
  - Demonstrate common motions
- [Jest](https://marketplace.visualstudio.com/items?itemName=orta.vscode-jest)
  - Install Jest
  - Create example test, show in-editor status updates
  - Debug
- [Starship](https://starship.rs/)
