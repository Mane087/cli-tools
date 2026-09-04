| **Command**                                                        | **What it does**                                                                                 |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `rg usuario`                                                       | Recursively searches for `usuario` from the current directory.                                   |
| `rg IDLOTE ./priv/sql`                                             | Searches for `IDLOTE` only inside `./priv/sql`.                                                  |
| `rg IDLOTE ./priv/sql/lotes.sql`                                   | Searches for `IDLOTE` in a specific file.                                                        |
| `rg IDLOTE ./lib ./priv/sql ./test`                                | Searches for `IDLOTE` across multiple directories.                                               |
| `rg -F 'user.id'`                                                  | Searches for the exact literal string `user.id` without interpreting it as a regular expression. |
| `rg -i usuario`                                                    | Performs a case-insensitive search.                                                              |
| `rg -s Usuario`                                                    | Forces a case-sensitive search.                                                                  |
| `rg -S usuario`                                                    | Uses smart case: case-insensitive unless the pattern contains uppercase letters.                 |
| `rg -w status`                                                     | Matches `status` only as a complete word.                                                        |
| `rg -x 'COMMIT;'`                                                  | Matches only lines whose entire contents are `COMMIT;`.                                          |
| `rg -e ERROR -e WARNING -e FATAL`                                  | Searches for multiple patterns in a single command.                                              |
| `rg -v DEBUG app.log`                                              | Shows lines that do not match `DEBUG`.                                                           |
| `rg usuario -g '*.ex'`                                             | Searches only in files with the `.ex` extension.                                                 |
| `rg usuario -g '*.ex' -g '*.exs'`                                  | Searches only in `.ex` and `.exs` files.                                                         |
| `rg usuario -g '!*.spec.ts'`                                       | Excludes files matching the `*.spec.ts` glob.                                                    |
| `rg usuario -g '!node_modules/**' -g '!dist/**' -g '!coverage/**'` | Excludes specified directories from the search.                                                  |
| `rg --hidden DATABASE_URL`                                         | Includes hidden files and directories in the search.                                             |
| `rg -u usuario`                                                    | Searches files ignored by `.gitignore` and other ignore rules.                                   |
| `rg -uu usuario`                                                   | Includes both hidden and ignored files.                                                          |
| `rg -C 2 'IDLOTE'`                                                 | Shows two lines before and after each match.                                                     |
| `rg -B 3 'ERROR' app.log`                                          | Shows three lines before each match.                                                             |
| `rg -A 3 'ERROR' app.log`                                          | Shows three lines after each match.                                                              |
| `rg -l IDLOTE`                                                     | Prints only the names of files containing matches.                                               |
| `rg -L IDLOTE`                                                     | Prints only the names of files that do not contain matches.                                      |
| `rg -n usuario`                                                    | Shows line numbers for each match.                                                               |
| `rg --no-heading usuario`                                          | Prints every match without grouping results by filename.                                         |
| `rg -o 'https?://[^ ]+'`                                           | Prints only the matching part of each line.                                                      |
| `rg -c ERROR`                                                      | Shows the number of matching lines per file.                                                     |
| `rg --count-matches ERROR`                                         | Shows the total number of individual matches per file.                                           |
| `rg '^ERROR' app.log`                                              | Finds lines that start with `ERROR`.                                                             |
| `rg 'COMMIT;$'`                                                    | Finds lines that end with `COMMIT;`.                                                             |
| `rg 'ERROR\|WARNING\|FATAL'`                                       | Searches for alternatives using a regular expression.                                            |
| `rg 'user_[0-9]+'`                                                 | Searches using a regular expression with a numeric pattern.                                      |
| `rg '\bTODO\b'`                                                    | Finds `TODO` as a complete word using regex word boundaries.                                     |
| `rg usuario -t elixir`                                             | Searches only files recognized by ripgrep as Elixir files.                                       |
| `rg usuario -t ts`                                                 | Searches only TypeScript files.                                                                  |
| `rg usuario -T js`                                                 | Searches all supported files except JavaScript files.                                            |
| `rg --type-list`                                                   | Lists all built-in file types recognized by ripgrep.                                             |
| `rg --files`                                                       | Lists files that ripgrep would search without searching their contents.                          |
| `rg --files -g '*.ex'`                                             | Lists only `.ex` files.                                                                          |
| `rg --files \| rg 'test'`                                          | Filters the searchable file list to paths containing `test`.                                     |
| `rg TODO --stats`                                                  | Searches for `TODO` and prints search statistics.                                                |
| `rg TODO --json`                                                   | Outputs search results as structured JSON.                                                       |
| `rg 'foo' --replace 'bar'`                                         | Shows matches with `foo` replaced by `bar` in the output without modifying files.                |
| `rg 'TODO\(([^)]+)\)' -r 'TASK: $1'`                               | Uses capture groups to transform matching output.                                                |
