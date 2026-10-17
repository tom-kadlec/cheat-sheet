# cut
`cut` extracts selected **fields**, **characters**, or **bytes** from each line of a file or piped input. Its main use is pulling columns from delimited text such as *CSV*, `/etc/passwd`, or command output

## Syntax
```
cut OPTION... [FILE...]
```

## Key options
| Option               | Purpose                                   | Example                                         |
| -------------------- | ----------------------------------------- | ----------------------------------------------- |
| -f N                 | Select field(s); default delimiter is TAB | cut -f1 file.txt                                |
| -d X                 | Set input delimiter                       | cut -d',' -f2 data.csv                          |
| -c N-M               | Select character positions                | cut -c1-10 file.txt                             |
| -b N-M               | Select byte positions                     | cut -b1-5 file.txt                              |
| -s                   | Suppress lines without the delimiter      | cut -d',' -f2 -s data.csv                       |
| --complement         | Print everything except the selection     | cut -d',' -f1 --complement data.csv             |
| --output-delimiter=X | Use a different output delimiter          | cut -d',' -f1,3 --output-delimiter=';' data.csv |

## Selecting fields
```bash
cut -f1 file.txt                 # First TAB-separated field
cut -f1,3 file.txt               # Fields 1 and 3
cut -f1-4 file.txt               # Fields 1 through 4
cut -f2- file.txt                # Field 2 through the end
cut -f-3 file.txt                # Fields 1 through 3
```
Field ranges may be open-ended: 2- means “from field 2 onward,” while -3 means “through field 3.”

## Custom delimiters
```bash
cut -d',' -f2 data.csv           # Second CSV column
cut -d':' -f1 /etc/passwd        # Usernames
cut -d':' -f1,7 /etc/passwd      # Username and shell
cut -d' ' -f2 file.txt           # Second space-separated field
```
The default delimiter is TAB, so -d is required for CSV, colon-separated files, spaces, and most other formats.

## Characters and bytes
```bash
cut -c1-10 file.txt              # First 10 characters
cut -c3- file.txt                # From character 3 to end
cut -c1,4,7 file.txt             # Characters 1, 4, and 7
cut -b1-5 file.txt               # First 5 bytes
```
Prefer `-c` over `-b` with UTF-8 text, because one character may occupy multiple bytes.

## Exclude columns
```bash
cut -d',' -f1,3 --complement data.csv
```
This prints every CSV field except fields 1 and 3.
