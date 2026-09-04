# Useful CLI Tools for Daily Development

A practical collection of modern command-line tools worth installing on Linux and macOS for everyday development.

## [zoxide](https://github.com/ajeetdsouza/zoxide)

A smarter `cd` replacement that learns which directories you use most frequently.

View [zoxide command examples](https://github.com/Mane087/cli-tools/blob/main/examples/zoxide.md).

### Why it is useful

* Jump to directories using partial names
* Gets more accurate as you use it
* Integrates well with modern shells
* Reduces the need to type long directory paths

## [fdfind (fd)](https://github.com/sharkdp/fd)

A simpler and faster alternative to `find` for common file and directory searches.

View [fd command examples](https://github.com/Mane087/cli-tools/blob/main/examples/fdfind.md).

### Why it is useful

* Cleaner syntax than `find`
* Sensible defaults for everyday searches
* Great for searching by filename, extension, or directory
* Works well with tools such as `fzf`

## [fzf](https://github.com/junegunn/fzf)

An interactive fuzzy finder for files, command history, processes, Git references, and more.

### Why it is useful

* Turns long terminal lists into searchable interactive interfaces
* Provides excellent shell integration
* Pairs well with tools such as `fd`, `rg`, and `git`
* Makes navigating large sets of results much faster

## [ripgrep (rg)](https://github.com/burntsushi/ripgrep)

A fast recursive text-search tool that respects `.gitignore` rules by default.

View [ripgrep command examples](https://github.com/Mane087/cli-tools/blob/main/examples/ripgrep.md).

### Why it is useful

* Excellent for searching across large codebases
* Better defaults than `grep -R`
* Supports regular expressions and file globs
* Automatically ignores files excluded by `.gitignore`

## [jq](https://github.com/jqlang/jq)

A command-line JSON processor for filtering, transforming, querying, and extracting structured data.

View [jq command examples](https://github.com/Mane087/cli-tools/blob/main/examples/jq.md).

### Why it is useful

* Essential when working with APIs and JSON logs
* Works particularly well with `curl`
* Useful for shell scripts and debugging
* Makes complex JSON responses easier to inspect and transform

## [gh (GitHub CLI)](https://github.com/cli/cli)

The official GitHub command-line tool for managing pull requests, issues, repositories, workflows, releases, and authenticated API requests.

View [GitHub CLI command examples](https://github.com/Mane087/cli-tools/blob/main/examples/gh.md).

### Why it is useful

* Manage pull requests and issues without leaving the terminal
* Authenticate both `gh` and Git operations
* Run and inspect GitHub Actions workflows
* Create and manage repositories from the command line
* Access the GitHub API without manually handling authentication

## [tree](https://github.com/peteretelej/tree)

A command-line utility that displays directories and files in a hierarchical tree structure.

It can recursively explore directories, limit traversal depth, include hidden files, display metadata, filter entries by pattern, and export results in formats such as HTML, XML, JSON, and CSV.

View [tree command examples](https://github.com/Mane087/cli-tools/blob/main/examples/tree.md).

### Why it is useful

* Quickly understand the structure of a project or directory
* Easier to read than recursive `ls` output
* Useful when documenting repository layouts
* Can limit output depth when working with large projects
* Supports filtering and multiple output formats for scripting and documentation

## [curl](https://github.com/curl/curl)

A command-line tool for transferring data using URL-based protocols. It is widely used for HTTP requests, APIs, file transfers, authentication, debugging, and automation.

View [curl command examples](https://github.com/Mane087/cli-tools/blob/main/examples/curl.md).

### Why it is useful

* Quickly test HTTP endpoints and REST APIs
* Send custom headers, request bodies, and authentication credentials
* Download and upload files directly from the terminal
* Inspect HTTP responses and troubleshoot network requests
* Works well with `jq` for processing JSON responses
* Easy to integrate into shell scripts, CI pipelines, and automation workflows
