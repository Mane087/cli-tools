| **Command**                   | **What it does**                                                                            |
| ----------------------------- | ------------------------------------------------------------------------------------------- |
| `z projects`                  | Jumps to the highest-ranked directory matching `projects`.                                  |
| `z projects cli tools`        | Searches for a directory matching multiple terms and jumps to the best match.               |
| `z`                           | Jumps to your home directory.                                                               |
| `zi`                          | Opens an interactive directory selector, usually powered by `fzf`.                          |
| `zi lynx`                     | Opens the interactive selector pre-filtered with `lynx`.                                    |
| `z -`                         | Jumps back to the previous directory.                                                       |
| `zoxide query -l`             | Lists all directories currently stored in zoxide's database.                                |
| `zoxide query -ls`            | Lists stored directories together with their ranking scores.                                |
| `zoxide query lynxwebex`      | Prints the best matching path without changing directories.                                 |
| `zoxide query -a lynxwebex`   | Prints the absolute path of the best matching directory.                                    |
| `zoxide query -i`             | Opens an interactive selector and prints the selected path.                                 |
| `zoxide add /path/to/project` | Manually adds a directory to zoxide's database.                                             |
| `zoxide remove /old/path`     | Removes a directory from zoxide's database.                                                 |
| `zoxide edit`                 | Opens the zoxide database in an interactive editor when supported by the installed version. |
| `z src`                       | Jumps to the most relevant previously visited directory matching `src`.                     |
| `z backend api`               | Jumps to the directory that best matches both `backend` and `api`.                          |
| `zoxide query -l \| rg lynx`  | Filters registered zoxide paths using `ripgrep`.                                            |
| `zoxide query -l \| fzf`      | Lets you manually fuzzy-search through all registered paths.                                |
