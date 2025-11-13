# Everyday-Commands

# File System Cheat Sheet  
### Navigation & Modification (Linux/macOS)

---

## File System Navigation

| Command | Description |
|--------|-------------|
| `pwd` | **P**rint **W**orking **D**irectory – show current path |
| `ls` | **L**i**s**t directory contents |
| `ls -a` | List **all** (including hidden files starting with `.`) |
| `ls -l` | **L**ong listing (permissions, owner, size, date) |
| `ls -la` or `ls -l -a` | Long listing **with hidden files** |
| `ls -r` | List in **reverse order** |
| `ls -lar` | Reverse + all + long (common combo) |
| `cd` | Change to **home directory** |
| `cd ~` | Same as `cd` – go home |
| `cd [dirname]` | Change to specific directory |
| `cd ..` | Go **up** one level (parent) |
| `cd -` | Go to **previous directory** (not always parent!) |
| `find /path -name "filename"` | **Find** file by name (case-sensitive) |
| `find . -name "*.log"` | Find all `.log` files in current dir |

**Pro Tip**: Combine flags: `ls -lah` = long, all, **human-readable** sizes

---

## Modifying Files & Directories

| Command | Description |
|--------|-------------|
| `mkdir [dirname]` | **M**a**k**e **dir**ectory |
| `mkdir -p /path/to/nested/dir` | Create parent dirs if they don't exist |
| `touch [filename]` | Create empty file (or update timestamp) |
| `rm [filename]` | **R**e**m**ove file |
| `rm -i [filename]` | Remove with **confirmation prompt** |
| `rm -r [dirname]` | Remove **directory** (recursive) |
| `rm -rf [dirname]` | **Force remove directory + contents** (dangerous!) |
| `rm ./*` | Remove **everything** in current folder |
| `cp [src] [dest]` | **C**o**p**y file |
| `cp -r [dir] [dest]` | Copy **directory** recursively |
| `mv [src] [dest]` | **M**o**v**e or **rename** file/directory |
| `mv file.txt newname.txt` | Rename file |
| `mv file.txt /new/path/` | Move file |
| `mv dir1/ dir2/` | Move/rename directory |
| `mv [src] [dest] -v` | Move with **verbose** output |

---

## Combine Commands with `&&`

Run multiple commands **only if the previous succeeds**:

```bash
mkdir backup && cp *.txt backup/ && echo "Backup complete!"
