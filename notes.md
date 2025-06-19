# Week 1 Linux Notes

## Absolute vs Relative Paths
- **Absolute Path**: Full path from root `/`
  - Example: `/home/user/Week1-Linux-Practice/files/data.txt`
- **Relative Path**: Path from the current working directory
  - Example: `./files/data.txt` (if you are in `Week1-Linux-Practice`)

> Use `pwd` to see your current directory and `cd` to navigate.

---

## File Permissions (rwx)
- **r** = read, **w** = write, **x** = execute
- Permissions are assigned for:
  - **User (u)** - owner
  - **Group (g)** - group
  - **Others (o)** - other

### Example: `-rwxr-xr--`
| Who       | Permissions | Description             |
|-----------|-------------|-------------------------|
| User      | rwx         | Can read/write/execute  |
| Group     | r-x         | Can read/execute        |
| Others    | r--         | Can only read           |

### Modify permissions:
```bash
chmod u+x script.sh      # Add execute permission to user
chmod 755 script.sh      # rwxr-xr-x
chmod -R 700 folder/     # Recursive permission set
