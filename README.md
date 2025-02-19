# File-Permissions-in-Linux

## Objective
The objective of this project was to enhance system security by properly configuring file and directory permissions in a Linux environment. By analyzing existing permissions and making necessary modifications, I ensured that sensitive files and directories had the appropriate access controls.

## Skills Learned
- Understanding and interpreting Linux file permission strings.
- Using `ls -la` to inspect file and directory permissions.
- Applying `chmod` to modify file and directory permissions.
- Managing access control to enforce security best practices.

## Tools Used
- **Linux Command Line (CLI)** for executing permission-related commands.
- **`ls -la`** for viewing file and directory permissions.
- **`chmod`** for modifying access rights.

## Steps

### Check File and Directory Details
**Ref 1: Listing files and their permissions using `ls -la`.**
```sh
ls -la /path/to/projects
```

### Describe the Permissions String
**Ref 2: Understanding permission breakdown.**
```plaintext
-rw-rw-r--  1 user group 1024 Feb 10 12:34 project_t.txt
```
- `-rw-rw-r--`:
  - `r` (read), `w` (write), `x` (execute) permissions for user, group, and others.
  - User and group have read and write access, others have read access only.

### Change File Permissions
**Ref 3: Removing write access for others using `chmod`.**
```sh
chmod o-w project_k.txt
```

### Change File Permissions on a Hidden File
**Ref 4: Preventing write access while keeping read access for user and group.**
```sh
chmod u-w,g-w,g+r .project_x.txt
```

### Change Directory Permissions
**Ref 5: Restricting directory access to a specific user.**
```sh
chmod 700 drafts
```

## Summary
This project reinforced my understanding of Linux file permissions and their role in securing system resources. By utilizing `ls -la` and `chmod`, I effectively managed access control to align with security policies.
```
