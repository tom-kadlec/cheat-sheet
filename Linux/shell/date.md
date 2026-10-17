# date

```bash
#!/bin/bash
today=$(date +%Y-%m-%d)
echo $today
```

| **Format** | **Description**                                                       | **Example code** | **Sample Output**               |
| ---------- | --------------------------------------------------------------------- | ---------------- | ------------------------------- |
| **%%**     | A literal                                                             | $ date +%%       | %                               |
| **%a**     | Locale’s weekday name in shorter form; Such as Sun                    | $ date +%a       | Sun                             |
| **%A**     | Locale’s full weekday name; Such as Sunday                            | $ date +%A       | Sunday                          |
| **%b**     | Locale’s month name in shorter form                                   | $ date +%b       | Jun                             |
| **%B**     | Locale’s full month name                                              | $ date +%B       | June                            |
| **%c**     | Locale’s date and time                                                | $ date +%c       | Sun 18 Jun 2023 12:18:40 PM +06 |
| **%C**     | century                                                               | $ date +%C       | 20                              |
| **%e**     | Day of month                                                          | $ date +%e       | 18                              |
| **%F**     | Full date; same as %Y-%m-%d                                           | $ date +%F       | 2023-06-18                      |
| **%g**     | Last two digits of the year of ISO week number                        | $ date +%g       | 23                              |
| **%G**     | year of ISO week number                                               | $ date +%G       | 2023                            |
| **%d**     | Day of month                                                          | $ date +%d       | 18                              |
| **%D**     | Date; same as %m/%d/%y                                                | $ date +%D       | 06/18/23                        |
| **%H**     | Hour                                                                  | $ date +%H       | 11                              |
| **%I**     | Hour                                                                  | $ date +%I       | 11                              |
| **%j**     | Day of year                                                           | $ date +%j       | 169                             |
| **%m**     | Month of year                                                         | $ date +%m       | 06                              |
| **%M**     | Minute(00 to 59)                                                      | $ date +%M       | 32                              |
| **%r**     | Locale’s 12-hour clock time                                           | $ date +%r       | 11:12:14 AM                     |
| **%q**     | Quarter of a year                                                     | $ date +%q       | 2                               |
| **%s**     | seconds since 1970-01-01 00:00:00 UTC                                 | $ date +%s       | 1687068749                      |
| **%S**     | seconds(00 to 60)                                                     | $ date +%S       | 50                              |
