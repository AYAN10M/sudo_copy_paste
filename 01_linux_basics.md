# Linux Command Line : Shell & Terminal

---

## 1. Shell : Definition and Role

### Shell

- A **shell** is a **program** that accepts **keyboard input** (commands) and passes them to the **operating system** for execution.
- It acts as a **command interpreter** between the user and the OS.
- When referring to the _command line_, we are effectively referring to the **shell**.

### Bash

- Most Linux distributions provide **bash** as the default shell.
- **bash** stands for **Bourne Again SHell**.
- It is an enhanced replacement for **sh** (the original Unix shell).
- The original **sh** was written by **Steve Bourne**.
- bash is part of the **GNU Project**.

---

## 2. Terminal Emulator : Purpose and Context

### Terminal Emulator

- A **terminal emulator** is required when working in a **graphical user interface (GUI)**.
- It provides a window that allows interaction with the shell.
- Its function is purely to **give access to the shell**.

### Common Examples

- KDE → **konsole**
- GNOME → **gnome-terminal** (often labeled simply _Terminal_)
- Multiple terminal emulators exist; functional differences are mostly related to features, not capability.

---

## 3. Shell Prompt

### Prompt Structure

Example:

```
[me@linuxbox ~]$
```

Typical components:

- `me` → username
- `linuxbox` → machine (host) name
- `~` → current working directory (home directory)
- `$` → indicates a regular (non-privileged) user

### Privileged Prompt

- A prompt ending with `#` indicates **superuser (root) privileges**.
- This occurs when:
  - Logged in as the root user, or
  - Using a terminal emulator configured for administrative access

---

## 4. Command Entry and Error Handling

### Command Execution

- The shell waits at the prompt until input is entered.
- Upon pressing **Enter**, the shell attempts to execute the command.

### Invalid Commands

Example:

```
kaekfjaeifj
```

Result:

```
bash: kaekfjaeifj: command not found
```

- Indicates the shell could not locate a command with that name.
- The shell then returns to the prompt, ready for new input.

---

## 5. Command History

### Command History

- The shell maintains a **history of previously executed commands**.
- By default, most Linux distributions store **approximately 1,000 commands**.

### Navigation

- **Up Arrow** → recall previous commands
- **Down Arrow** → move forward in history

---

## 6. Cursor Movement and Line Editing

### Line Editing

- Left and right arrow keys allow cursor movement within the command line.
- Enables modification of commands before execution.
- Supports efficient correction and reuse of previous input.

---

## 7. Mouse Interaction and Focus Behavior

### X Window System Copy–Paste

- The **X Window System** provides selection-based copy and paste:
  - Selecting text with the mouse copies it to an internal buffer
  - Pressing the **middle mouse button** pastes the buffer contents

### Control Keys

- `Ctrl+C` and `Ctrl+V` do **not** perform copy/paste in the terminal.
- These key combinations have predefined meanings within the shell and predate modern GUI conventions.

### Focus Policy

- **Click to focus**: window receives input only after being clicked
- **Focus follows mouse**: window receives input when the mouse pointer enters it
- Focus behavior is configurable via the window manager settings

---

## 8. Basic Commands Introduced

### `date`

- Displays the current system date and time

Example output:

```
Fri Feb 2 15:09:41 EST 2018
```

---

### `cal`

- Displays a calendar
- Default behavior shows the current month

---

## 9. Virtual Consoles

### Virtual Consoles

- Linux systems maintain multiple **text-based terminal sessions** independent of the GUI.
- These sessions remain active even when no terminal emulator is open.

### Access

- `Ctrl + Alt + F1` through `Ctrl + Alt + F6` → access virtual consoles
- Login is required upon access

### Switching

- `Alt + F1` through `Alt + F6` → switch between consoles
- `Alt + F7` → return to the graphical desktop (on most systems)

---

## 10. Disk Space Information

### `df`

- Displays disk space usage for mounted filesystems

Information shown:

- Filesystem name
- Total size
- Used space
- Available space
- Mount point

---

## 11. Memory Usage Information

### `free`

- Displays system memory usage

Information shown:

- Total memory
- Used memory
- Free memory
- Buffer and cache usage
- Swap space

---

## 12. Ending a Terminal Session

### Methods

- Close the terminal emulator window
- Execute the command:

```
exit
```

- Press:

```
Ctrl + D
```
