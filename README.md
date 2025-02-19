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

Check file and directory details

This code shows how I used Linux commands to check the current permissions of a directory.

![image](https://github.com/user-attachments/assets/65704985-0cc5-43a0-89ed-9ddbd1edf3ce)


The first line in the screenshot shows the command I entered, and the rest show the output. The command lists all files in the projects directory. I used `ls -la` to display a detailed list, including hidden files. The output shows one directory (`drafts`), one hidden file (`.project_x.txt`), and five other project files. The 10-character string in the first column represents each file or folder's permissions.
## Describe the permissions string
The 10-character string shows who can access a file and their permissions:
⦁	1st character: Indicates file type. A `d` means it's a directory, while `-` means it's a regular file.

⦁	2nd-4th characters: Show read (`r`), write (`w`), and execute (`x`) permissions for the file owner/User. A `-` means the permission is not granted.

⦁	5th-7th characters: Indicate the same permissions for the group.

⦁	8th-10th characters: Show permissions for other users on the system. A - means that permission is not allowed.

For example, the file permissions for `project_t.txt` are `-rw-rw-r--`. The first character is (`-`), meaning it's a file, not a directory. The `r` in the second, fifth, and eighth positions shows that the user, group, and others have read access. The `w` in the third and sixth positions means only the user and group can write to the file. No one has execute permissions.

## Change file permissions
The organization decided that others shouldn't have write access to any files. To follow this rule, I checked the file permissions and found that `project_k.txt` needed write access removed for others.

The following code demonstrates how I completed this task using Linux commands:

 ![image](https://github.com/user-attachments/assets/1b1657db-0125-4fd0-8454-969d74902f9f)


The first two lines of the screenshot show the commands I entered, and the rest show the output. The chmod command modifies file and directory permissions. The first argument specifies the permission change, and the second names the file or directory. In this example, I removed write permissions for others on `project_k.txt.` Then, I used `ls -la` to check the updates.

## Change file permissions on a hidden file
The research team at my organization archived `project_x.txt` and wants to prevent anyone from having write access. However, the user and group should still have read access.

This code shows how I used Linux commands to accomplish this:

 ![image](https://github.com/user-attachments/assets/ad3470bd-6ea4-4d2c-9f6c-1f4f2e96092a)

The first two lines in the screenshot show the commands I entered, and the rest show the output. I know `.project_x.txt` is hidden because its name starts with a period (`.`). In this example, I removed write permissions for the user and group and added read permissions for the group. I did this using `u-w` to remove write access for the user, `g-w` to remove it for the group, and `g+r` to add read access for the group.

## Change directory permissions
My organization wants only the researcher2 user to access the drafts directory and its contents. No one else should have execute permissions.

This code shows how I used Linux commands to modify permissions:

 ![image](https://github.com/user-attachments/assets/eb919447-fc88-4c9d-aa58-d87fc0ad4eb2)

The first two lines of the screenshot show the commands I entered, and the rest show the output. Since the group had execute permissions, I used the chmod command to remove them. The researcher2 user already had execute permissions, so no changes were needed for them.



## Summary
This project reinforced my understanding of Linux file permissions and their role in securing system resources. By utilizing `ls -la` and `chmod`, I effectively managed access control to align with security policies.
