# 🧙‍♂️ LogWizard

LogWizard is a fast, intuitive Python CLI tool for analyzing and filtering log files — built for developers, sysadmins, and curious tinkerers.

---

## 🚀 Features

- 📂 Load & remember a log file for all future commands
- 🔍 Filter logs by level, keyword, or timestamp
- 📈 Count entries by level, day, or hour
- 🧠 Find the most common error message
- 👀 Preview the first 10 lines of any log file
- 🖍️ Colorized terminal output
- 🧪 `--help` available for every command
- 🌠 Short aliases for power users (e.g. `lw v` for view)

---

## 🛠️ Installation

1. Clone the repo:

```bash
git clone https://github.com/therealoganh/logwizard.git
cd logwizard
```

2. (Optional) Set an alias for global usage:

```bash
alias lw='python logwizard.py'
```

Now you can run:

```bash
lw l logs/system.log
lw v --level ERROR --after "2025-06-01"
```

---

## 📘 Usage Examples

| Action                   | Command                                   |
| ------------------------ | ----------------------------------------- |
| Load a file              | `lw l logs/system.log`                    |
| View filtered logs       | `lw v --level ERROR --after "2025-06-01"` |
| Count all lines          | `lw ln`                                   |
| Count logs on a day/hour | `lw ln --day "2025-06-25" --hour 13`      |
| View log level breakdown | `lw lv`                                   |
| Find most common error   | `lw e`                                    |
| Clear saved file         | `lw c`                                    |

---

## 🔍 Available Commands

- `load` / `l` - Load and remember a log file
- `clear` / `c` - Clear remembered file
- `preview` / `p` - Preview first 10 lines
- `view` / `v` - View logs with filters:
  - `--level`, `--keyword`, `--before`, `--after`
- `lines` / `ln` - Count lines optionally by day/hour
- `levels` / `lv` - Count log entries by severity
- `mce` / `e` - Print most common error

---

## 🧠 Developer Notes

This project uses:

- [Click](https://palletsprojects.com/p/click/) for CLI scaffolding
- Modular logic in `wiz_logic.py`
- `.logwizard` file to store the current working file
- Helpful error handling and exit codes
- Colorful output with `click.secho` for readability
- ### 📝 .logwizard file

This file is created automatically to remember the last loaded log file path. It's local to your system and included in `.gitignore`.


---

## 👨‍💻 Author

Built by Logan Hill — A passionate Python developer experimenting with CLI tools and new libraries.

