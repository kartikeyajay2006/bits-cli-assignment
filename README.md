# 🐧 Linux Command-Line Lab: Graded Assignment (Modules 1–4)

**BITS Pilani graded lab: five hands-on Linux investigations. Each one comes with the exact commands run, their real output, screenshots and a written report.**

## The five investigations

| # | Topic | What was done | Report |
|---|---|---|---|
| 1 | **Environment and identity** | Inspected the user, groups, shell, working directory and network reachability (`whoami`, `id`, `groups`, `$SHELL`, `pwd`, `ls -la`, `ping`) | [Environment_Report](Question1/Environment_Report.txt) |
| 2 | **Project workspace and permissions** | Built a workspace, wrote plans and notes in `vi`, then locked it down with `chmod 750` and checked `umask` and `find` | [Project_Workspace_Report](Question2/Project_Workspace_Report.txt) |
| 3 | **Hard links vs symbolic links** | Created both, compared inode numbers and link counts with `stat`, and deleted the target to see which link survives | [Link_Analysis_Report](Question3/Link_Analysis_Report.txt) |
| 4 | **I/O, file descriptors and limits** | Inspected open descriptors with `lsof -p`, sent stdout and stderr to `output.txt` and `error.txt`, and checked `ulimit -a` | [IO_Investigation_Report](Question4/IO_Investigation_Report.txt) |
| 5 | **Storage assessment** | Disks, mounts, space and inode usage, and disk health (`lsblk`, `df -h`, `df -i`, `mount`, `smartctl -H`), with the report written in `vi` | [Storage_Assessment_Report](Question5/Storage_Assessment_Report.txt) |

## Layout

```text
QuestionN/
  Commands_And_Observations.md   every command, its output, and what it shows
  *_Report.txt                   the written report
  coursera_command_output.txt    raw terminal transcript
  Screenshots/                   proof of execution
```

## Key takeaways

- A **hard link** is another name for the same inode, so it survives deletion of the original. A **symlink** stores a path, so it breaks.
- `2>` and `>` are independent streams. `>>` appends and `>` truncates.
- `df` reports filesystems, `lsblk` reports block devices, and `lsof` shows which process holds a file.

See also: [Linux-Lab-Assignment-BITS](https://github.com/kartikeyajay2006/Linux-Lab-Assignment-BITS), the shell-scripting lab.

## Author

**[Kartikeya Yadav](https://github.com/kartikeyajay2006)** · BITS Pilani
