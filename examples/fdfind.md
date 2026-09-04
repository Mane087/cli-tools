| **Command**                            | **What it does**                                                        |
| -------------------------------------- | ----------------------------------------------------------------------- |
| `fdfind usuario`                       | Search for files and directories whose name contains `usuario`.         |
| `fdfind -e sql`                        | Search for files with the `.sql` extension.                             |
| `fdfind config -t f`                   | Search only for files matching `config`.                                |
| `fdfind migrations -t d`               | Search only for directories matching `migrations`.                      |
| `fdfind -H '.env'`                     | Include hidden files and directories in the search.                     |
| `fdfind -u archivo`                    | Include hidden files and files ignored by `.gitignore`.                 |
| `fdfind -e ts -E node_modules -E dist` | Search for TypeScript files while excluding `node_modules` and `dist`.  |
| `fdfind -p 'controllers/.*\.ex$'`      | Match against the full path instead of only the filename.               |
| `fdfind -e log -x gzip`                | Execute `gzip` once for each `.log` file found.                         |
| `fdfind -e ts -X code`                 | Pass all matching TypeScript files to a single `code` command.          |
| `fdfind -e sql -X rg 'IDLOTE'`         | Search for `IDLOTE` inside all `.sql` files found.                      |
| `fdfind --changed-within 1d`           | Find files modified within the last day.                                |
| `fdfind --changed-before 7d`           | Find files modified more than seven days ago.                           |
| `fdfind -t f --size +100m`             | Find files larger than 100 MB.                                          |
| `fdfind -t f --size -1m`               | Find files smaller than 1 MB.                                           |
| `fdfind config .`                      | Search for `config` starting from the current directory.                |
| `fdfind config src/`                   | Search for `config` only inside the `src` directory.                    |
| `fdfind -d 2`                          | Limit the search to a maximum depth of two directories.                 |
| `fdfind -d 1 -t d`                     | List directories only one level below the current directory.            |
| `fdfind -g '*.test.ts'`                | Search using a glob pattern.                                            |
| `fdfind -g 'package*.json'`            | Find files matching the `package*.json` glob pattern.                   |
| `fdfind '^README'`                     | Find files or directories whose name starts with `README`.              |
| `fdfind '\.env$'`                      | Find entries whose name ends with `.env`.                               |
| `fdfind -i readme`                     | Perform a case-insensitive search for `readme`.                         |
| `fdfind -s README`                     | Perform a case-sensitive search for `README`.                           |
| `fdfind -L package.json`               | Follow symbolic links while searching.                                  |
| `fdfind -t l`                          | Search only for symbolic links.                                         |
| `fdfind -t x`                          | Search only for executable files.                                       |
| `fdfind -e tmp -x rm`                  | Delete every `.tmp` file found.                                         |
| `fdfind -e log -x rm`                  | Delete every `.log` file found.                                         |
| `fdfind -e js -X wc -l`                | Count lines across all matching JavaScript files.                       |
| `fdfind -e md -X grep -l 'TODO'`       | Find Markdown files and show those containing `TODO`.                   |
| `fdfind -0 -e txt \| xargs -0 wc -l`   | Safely pass matching files to `xargs`, including filenames with spaces. |
