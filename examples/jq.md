| **Command**                                              | **What it does**                                          |
| -------------------------------------------------------- | --------------------------------------------------------- |
| `jq '.' file.json`                                       | Pretty-print a JSON file.                                 |
| `jq '.name' file.json`                                   | Extract the value of the `name` field.                    |
| `jq '.user.name' file.json`                              | Extract a nested field.                                   |
| `jq '.items[0]' file.json`                               | Get the first element of an array.                        |
| `jq '.items[-1]' file.json`                              | Get the last element of an array.                         |
| `jq '.items[]' file.json`                                | Iterate over every element in an array.                   |
| `jq '.items \| length' file.json`                        | Count the number of elements in an array.                 |
| `jq 'keys' file.json`                                    | List the keys of a JSON object.                           |
| `jq 'has("name")' file.json`                             | Check whether an object contains the `name` key.          |
| `jq '.name // "Unknown"' file.json`                      | Return a default value when a field is missing or `null`. |
| `jq '.users[] \| .name' file.json`                       | Extract the `name` field from every object in an array.   |
| `jq '.users[] \| select(.active == true)' file.json`     | Filter objects based on a condition.                      |
| `jq '.users[] \| select(.age > 18)' file.json`           | Filter objects using a numeric comparison.                |
| `jq '.users \| map(.name)' file.json`                    | Create an array containing only selected fields.          |
| `jq '.users \| map(select(.active))' file.json`          | Filter an array and return the matching objects.          |
| `jq '.users \| sort_by(.name)' file.json`                | Sort objects by a field.                                  |
| `jq '.users \| reverse' file.json`                       | Reverse the order of an array.                            |
| `jq '.users \| unique_by(.email)' file.json`             | Remove duplicate objects based on a field.                |
| `jq '{name: .name, email: .email}' file.json`            | Create a new object with selected fields.                 |
| `jq '.name = "John"' file.json`                          | Replace the value of a field in the output.               |
| `jq '.count += 1' file.json`                             | Increment a numeric field.                                |
| `jq 'del(.password)' file.json`                          | Remove a field from an object.                            |
| `jq '. + {"active": true}' file.json`                    | Add a new field to an object.                             |
| `jq -r '.name' file.json`                                | Output a string without JSON quotes.                      |
| `jq -c '.' file.json`                                    | Output compact JSON on a single line.                     |
| `jq -S '.' file.json`                                    | Sort object keys alphabetically.                          |
| `jq -e '.success' file.json`                             | Set the command exit status based on the JSON result.     |
| `jq --arg name "John" '.name = $name' file.json`         | Pass a shell string variable safely into a jq filter.     |
| `jq --argjson count 10 '.count = $count' file.json`      | Pass a JSON value or number into a jq filter.             |
| `curl -s https://api.example.com/users \| jq '.'`        | Pretty-print a JSON response from an HTTP API.            |
| `curl -s https://api.example.com/users \| jq '.[].name'` | Extract a field from every object returned by an API.     |
