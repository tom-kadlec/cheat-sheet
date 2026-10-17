# grep
## Search string in files
```shell
$ grep -rn example
```
`-r` search recursively
`-n` show line number
`-o` only show matching text (don’t return the whole line)

## Invert match
```
grep -v
```
or
```
grep --invert-match
```

## Regex modes
| Option | Regex type | Example |
| ------ | -------------------------- | ----------------------- |
| `-G` | Basic regex (BRE), default | `grep 'err\|warn' file` |
| `-E` | Extended regex (ERE) | `grep -E 'err|warn' file` |
| `-F` | Fixed string, no regex | `grep -F 'a.b' file` |
| `-P` | Perl-compatible regex (PCRE), GNU grep | `grep -P '\d{3}-\d{4}' file` |

`-E` avoids escaping alternation and quantifiers; -F is best when searching literal text containing regex metacharacters.
