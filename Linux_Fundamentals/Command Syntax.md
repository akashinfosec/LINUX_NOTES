# Command Syntax

## Command [Options] [Arguments]

- **Command** = The program we want to run.

- **Options** = Modify the behaviour of the command.
  - `-` = Short option (e.g., `-a`)
  - `--` = Long option (e.g., `--all`)

- **Arguments** = The target on which the command operates (files, directories, users, etc.).

### Example

```bash
ls -la /var/log
```

- **Command** → `ls`
- **Options** → `-la` (`-l` + `-a`)
- **Argument** → `/var/log`

### NOTE:
```note
man ls
```

- ` **man ls** ` command opens the manual for `ls` command
