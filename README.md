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

## Curl

It is a command-line tool for transferring data with URL syntax. It supports many protocols and is commonly used for HTTP APIs, file downloads, uploads, authentication, headers, debugging, and scripting.

## Basic syntax

```bash
curl [options] [URL...]
```

## Most useful curl commands

| Use case                           | Command                                                                                                        | What it does                                                            |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Basic GET request                  | `curl https://api.example.com/users`                                                                           | Sends a simple GET request and prints the response body.                |
| Save response to a file            | `curl -o users.json https://api.example.com/users`                                                             | Downloads the response and saves it with a chosen filename.             |
| Keep remote filename               | `curl -O https://example.com/archive.tar.gz`                                                                   | Downloads a file and preserves the remote filename.                     |
| Follow redirects                   | `curl -L https://example.com`                                                                                  | Follows HTTP 3xx redirects automatically.                               |
| Show headers only                  | `curl -I https://example.com`                                                                                  | Sends a HEAD request and prints response headers.                       |
| Show request and response details  | `curl -v https://example.com`                                                                                  | Enables verbose mode for troubleshooting connections and headers.       |
| Fail on HTTP errors                | `curl -f https://api.example.com/users/999`                                                                    | Returns an error exit code on HTTP 400/500 responses.                   |
| Silent mode with errors kept       | `curl -sS https://api.example.com/users`                                                                       | Hides progress output but still prints errors.                          |
| Pretty good default for scripts    | `curl -fsS https://api.example.com/health`                                                                     | Combines fail, silent, and show-error behavior.                         |
| Send JSON with POST                | `curl -X POST https://api.example.com/users -H "Content-Type: application/json" -d '{"name":"Ana"}'`           | Sends a JSON request body using POST.                                   |
| Send JSON with PUT                 | `curl -X PUT https://api.example.com/users/42 -H "Content-Type: application/json" -d '{"name":"Ana Updated"}'` | Replaces or updates a resource with a JSON payload.                     |
| Send PATCH request                 | `curl -X PATCH https://api.example.com/users/42 -H "Content-Type: application/json" -d '{"role":"admin"}'`     | Partially updates a resource.                                           |
| Send DELETE request                | `curl -X DELETE https://api.example.com/users/42`                                                              | Deletes a resource.                                                     |
| Add custom header                  | `curl -H "Authorization: Bearer <token>" https://api.example.com/me`                                           | Sends a custom HTTP header, commonly for auth.                          |
| Send multiple headers              | `curl -H "Accept: application/json" -H "X-Trace-Id: 123" https://api.example.com/me`                           | Adds more than one header to the request.                               |
| Send query parameters              | `curl "https://api.example.com/search?q=term&page=1"`                                                          | Makes a request with query string parameters.                           |
| URL-encode form field              | `curl -G --data-urlencode "q=hello world" https://api.example.com/search`                                      | Sends URL-encoded query parameters safely.                              |
| Submit form data                   | `curl -d "username=demo&password=secret" https://example.com/login`                                            | Sends `application/x-www-form-urlencoded` data.                         |
| Multipart file upload              | `curl -F "file=@report.pdf" https://api.example.com/upload`                                                    | Uploads a file as multipart form data.                                  |
| Upload multiple form fields        | `curl -F "file=@report.pdf" -F "type=invoice" https://api.example.com/upload`                                  | Uploads files and regular form fields together.                         |
| Basic auth                         | `curl -u user:password https://api.example.com/me`                                                             | Uses HTTP Basic Authentication.                                         |
| Bearer token auth                  | `curl -H "Authorization: Bearer <token>" https://api.example.com/me`                                           | Uses token-based authentication.                                        |
| Use a cookie jar                   | `curl -c cookies.txt https://example.com/login`                                                                | Stores cookies received from the server.                                |
| Send stored cookies                | `curl -b cookies.txt https://example.com/profile`                                                              | Reuses cookies from a previous request.                                 |
| Store and send cookies in one flow | `curl -c cookies.txt -b cookies.txt https://example.com/profile`                                               | Persists session state across requests.                                 |
| Download and resume                | `curl -C - -O https://example.com/large.iso`                                                                   | Resumes a partially downloaded file.                                    |
| Limit rate                         | `curl --limit-rate 1M -O https://example.com/large.iso`                                                        | Throttles download speed.                                               |
| Set timeout                        | `curl --connect-timeout 5 --max-time 30 https://example.com`                                                   | Limits connect time and total request time.                             |
| Retry transient failures           | `curl --retry 5 --retry-delay 2 https://example.com`                                                           | Retries failed transfers automatically.                                 |
| Ignore invalid TLS cert            | `curl -k https://dev.local`                                                                                    | Disables certificate verification. Useful only for local/dev scenarios. |
| Specify output format for metrics  | `curl -o /dev/null -s -w "HTTP %{http_code}\nTime %{time_total}s\n" https://example.com`                       | Prints status code and timing metrics.                                  |
| Use a proxy                        | `curl -x http://proxy.local:8080 https://example.com`                                                          | Sends the request through an HTTP proxy.                                |
| Read config from file              | `curl -K curl.conf https://example.com`                                                                        | Loads options from a config file.                                       |
| Fetch several URLs in one command  | `curl https://example.com https://curl.se`                                                                     | Requests multiple URLs in sequence in a single invocation.              |
| Parallel transfers                 | `curl --parallel -O https://example.com/a.zip -O https://example.com/b.zip`                                    | Downloads multiple URLs in parallel.                                    |

### Notes

* `curl` treats anything on the command line that is not an option or its argument as a URL.
* It can fetch multiple URLs in one invocation and can reuse connections within that same command.
* `-d` implies a POST request unless another method is specified.
* `-I` fetches headers only.
* `-L` is essential when a site redirects.
* `-k` is convenient in development, but using it casually in production is a bad security practice.
* For APIs, `-fsS` is usually a better default than plain `curl` in scripts because it fails on HTTP errors, hides the progress meter, and still shows errors.
