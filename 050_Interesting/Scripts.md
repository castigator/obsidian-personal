
```bash

❯ crontab -l
0 8,14,18 * * 1-5 PATH="$PATH:/opt/homebrew/bin/"; restic -r rclone:rupert-drive:restic --password-file=/Users/rupert.thomas/.script/restic-pass.txt backup --files-from /Users/rupert.thomas/.script/restic-files.txt >> /Users/rupert.thomas/cronlog.txt; restic -r rclone:rupert-drive:restic --password-file=/Users/rupert.thomas/.script/restic-pass.txt --group-by host forget --keep-last 3 >> /Users/rupert.thomas/cronlog.txt
```