# Useful CLI Tools for Daily Development

A practical markdown note with modern terminal tools that are worth installing on Linux/macOS.

## zoxide

A smarter `cd` replacement that learns your most frequently used directories.

**Why it is useful**

* Jump to directories by partial name
* Gets faster as you use it
* Works well with shell integrations

**Examples**

```bash
z project
zi
```

## fd / fdfind

A simpler and faster alternative to `find` for common file searches.

**Why it is useful**

* Cleaner syntax than `find`
* Sensible defaults
* Good for filenames, extensions, and scoped searches

**Examples**

```bash
fd docker
fd -e ts src
fd config /etc
```

## fzf

Interactive fuzzy finder for files, history, processes, git refs, and more.

**Why it is useful**

* Turns long terminal lists into searchable UIs
* Excellent shell integration
* Pairs well with `fd`, `rg`, and `git`

**Examples**

```bash
fd . | fzf
history | fzf
ps -ef | fzf
```

## ripgrep (rg)

Fast recursive text search that respects `.gitignore` by default.

**Why it is useful**

* Great codebase search tool
* Better defaults than `grep -R`
* Supports regex and file globs

**Examples**

```bash
rg "TODO"
rg "UserService" src
rg -t ts "interface"
rg -g "*.ex" "handle_event"
```

## jq

JSON processor for filtering, transforming, and extracting structured data.

**Why it is useful**

* Essential for APIs and logs
* Works perfectly with `curl`
* Good for scripts and debugging

**Examples**

```bash
curl -s http://localhost:3000/api/users | jq
jq '.data.items[] | {id, name}' response.json
jq -r '.token' auth.json
```
## gh (GitHub CLI)

Official GitHub command-line tool for pull requests, issues, repositories, workflows, and authenticated API calls.

**Why it is useful**

Good for PR and issue workflows without leaving the terminal
Can authenticate both gh and git
Useful for GitHub Actions, repo creation, and API scripting

Examples
```bash
gh auth login
gh auth setup-git
gh repo view
gh pr status
gh pr create
gh issue list
gh workflow list
gh api user
```

## Tree
It is a command-line utility that prints directories and files in a hierarchical tree format. It can recurse through subdirectories, show metadata, restrict depth, include hidden files, filter by patterns, and export output in formats such as HTML, XML, JSON, and CSV.

|  Coomand | Use |
|  ------ | ------ |
|  Show the current directory as a tree | tree |
|  Show a specific directory | tree ~/projects |
|  Limit recursion depth | tree -L 2 |
|  Show hidden files too | tree -a |
|  Show only directories | tree -d |
|  Include file sizes | tree -s |
|  Show permissions, owner, and group | tree -pug |
|  Sort by modification time | tree -t |
|  Do not descend into other filesystems | tree -x |
|  Match a pattern | tree -P "*.js" |
|  Ignore a pattern| tree -I "node_modules|.git" |
| Print full paths | tree -f |

---

## [Curl](https://github.com/curl/curl)

It is a command-line tool for transferring data with URL syntax. It supports many protocols and is commonly used for HTTP APIs, file downloads, uploads, authentication, headers, debugging, and scripting.

## [Curl commands examples](https://github.com/Mane087/cli-tools/blob/main/examples/curl.md)
