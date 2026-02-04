# Linux Navigation : Filesystem & Directory Movement

---

## 1. Navigation : Purpose

Navigation refers to **moving through the Linux filesystem** using the shell.
Core commands introduced:

- `pwd` : print current working directory
- `cd` : change directory
- `ls` : list directory contents

---

## 2. Filesystem Organization Model

### Hierarchical Directory Structure

- Linux uses a **hierarchical directory structure**.
- Files and directories are organized in a **tree-like form**.
- Directories may contain:
  - Files
  - Subdirectories

### Root Directory

- The **root directory** is the top of the filesystem tree.
- Represented by a single forward slash:

```
/
```

All other files and directories descend from root.

---

## 3. Single Filesystem Tree Concept

- Linux always presents **one unified filesystem tree**.
- This is independent of:
  - Number of disks
  - Number of storage devices

### Mounting

- Storage devices are **mounted** at directories within the tree.
- Mount points are determined by the system administrator.
- Unlike Windows, Linux does **not** create separate filesystem trees per drive.

---

## 4. Current Working Directory (CWD)

### Definition

- The **current working directory** is the directory in which the shell is currently operating.
- All relative path operations are evaluated from this directory.

### Initial State

- Upon login or terminal start, the CWD is set to the user’s **home directory**.
- Each user account has its own home directory.
- Regular users are permitted to write files only within locations they own (typically their home directory).

---

## 5. Displaying the Current Working Directory

### `pwd`

- Command: `pwd`
- Purpose: Displays the absolute path of the current working directory.

Example:

```
/home/me
```

---

## CWD vs `pwd`

### Key Distinction

- **CWD (Current Working Directory)**: A concept or state referring to the specific folder where a process (like your shell) is currently operating.
- **`pwd` (Print Working Directory)**: The command you run in your terminal to display the CWD.

## 6. Listing Directory Contents

### `ls`

- Command: `ls`
- Purpose: Lists files and directories contained in a directory.
- Default behavior: Lists contents of the current working directory.

### Targeted Listing

- `ls` may be applied to any directory by supplying a pathname.

---

## 7. Changing the Current Working Directory

### `cd`

- Command: `cd pathname`
- Purpose: Changes the current working directory to the specified location.

### Pathname

- A **pathname** is a sequence of directory names representing a route through the filesystem tree.
- Two pathname types exist:
  - Absolute pathnames
  - Relative pathnames

---

## 8. Absolute Pathnames

### Definition

- An **absolute pathname** begins at the root directory (`/`).
- It describes the complete path from root to the target.

### Example

```
/usr/bin
```

Interpretation:

- `/` → root directory
- `usr` → subdirectory of root
- `bin` → subdirectory of `/usr`

### Usage

```
cd /usr/bin
```

---

## 9. Relative Pathnames

### Definition

- A **relative pathname** begins from the current working directory.
- It does not start with `/`.

### Special Notations

- `.` → current working directory
- `..` → parent directory

---

## 10. Parent Directory Navigation

From `/usr/bin` to `/usr`:

### Absolute

```
cd /usr
```

### Relative

```
cd ..
```

Both methods produce identical results.

---

## 11. Subdirectory Navigation

From `/usr` to `/usr/bin`:

### Absolute

```
cd /usr/bin
```

### Relative

```
cd ./bin
```

### Implied Current Directory

- `./` is usually implied.
- The following is equivalent:

```
cd bin
```

If no pathname prefix is specified, the current working directory is assumed.

---

## 12. Filename Characteristics in Linux

### Hidden Files

- Filenames beginning with `.` are hidden.
- Hidden files are not shown by default with `ls`.
- They are typically used for configuration.

### Case Sensitivity

- Filenames are case sensitive.
- `File1` and `file1` represent different files.

### Filename Length and Characters

- Linux supports long filenames.
- Filenames may include punctuation and spaces.
- Recommended characters for portability:
  - Period (`.`)
  - Dash (`-`)
  - Underscore (`_`)

### Whitespace

- Spaces in filenames are supported but discouraged.
- Use underscores instead of spaces.

---

## 13. File Extensions

- Linux has **no inherent concept of file extensions**.
- File purpose and type are not determined by filename suffix.
- Some applications use extensions by convention, not by system requirement.

---

## 14. Directory Navigation Shortcuts

### Common `cd` Forms

| Command         | Result                                    |
| --------------- | ----------------------------------------- |
| `cd`            | Change to home directory                  |
| `cd -`          | Change to previous working directory      |
| `cd ~user_name` | Change to specified user’s home directory |

Example:

```
cd ~bob
```

---
