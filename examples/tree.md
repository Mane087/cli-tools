| **Command**                       | **What it does**                                                  |
| --------------------------------- | ----------------------------------------------------------------- |
| `tree`                            | Displays the current directory structure as a tree.               |
| `tree ~/projects`                 | Displays the contents of a specific directory as a tree.          |
| `tree -L 2`                       | Limits recursion to two directory levels.                         |
| `tree -a`                         | Includes hidden files and directories.                            |
| `tree -d`                         | Displays directories only.                                        |
| `tree -s`                         | Shows the size of each file in bytes.                             |
| `tree -h`                         | Shows file sizes in a human-readable format.                      |
| `tree -pug`                       | Shows permissions, owner, and group for each entry.               |
| `tree -t`                         | Sorts entries by modification time.                               |
| `tree -r`                         | Reverses the sort order.                                          |
| `tree -x`                         | Prevents traversal into directories located on other filesystems. |
| `tree -P "*.js"`                  | Displays only entries matching the specified pattern.             |
| `tree -I "node_modules\|.git"`    | Excludes entries matching the specified patterns.                 |
| `tree -f`                         | Prints the full path for each file and directory.                 |
| `tree --dirsfirst`                | Lists directories before files.                                   |
| `tree --du`                       | Shows the accumulated size of each directory.                     |
| `tree -L 3 -d`                    | Displays directories only, up to three levels deep.               |
| `tree -a -I ".git\|node_modules"` | Includes hidden files while excluding `.git` and `node_modules`.  |
| `tree -h -L 2`                    | Shows a two-level tree with human-readable file sizes.            |
| `tree -p -L 2`                    | Shows file permissions while limiting recursion depth.            |
| `tree -J`                         | Outputs the directory tree as JSON.                               |
| `tree -X`                         | Outputs the directory tree as XML.                                |
| `tree -H "." -o tree.html`        | Generates an HTML representation of the directory tree.           |
| `tree -J > tree.json`             | Saves the directory structure as JSON.                            |
| `tree -L 2 > structure.txt`       | Saves a two-level directory tree to a text file.                  |
