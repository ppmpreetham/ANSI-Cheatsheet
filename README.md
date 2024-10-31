# ANSI Escape Codes Cheatsheet

This cheatsheet covers ANSI escape codes for text formatting, colors, cursor control, and screen manipulation in terminal interfaces.

## Basic Structure
Each ANSI escape sequence follows the format:
```
\033[<code>m
```
- `\033` (or `\e` in some languages) is the escape character.
- `[<code>]` is the code for styling or color.
- `m` terminates the sequence.

## Text Formatting Codes

| Code | Description         |
|------|---------------------|
| 0    | Reset / Normal      |
| 1    | Bold / Bright       |
| 2    | Dim                 |
| 3    | Italic              |
| 4    | Underline           |
| 5    | Blink               |
| 7    | Inverse (Swap colors) |
| 8    | Hidden              |
| 9    | Strikethrough       |

### Reset Individual Effects
| Code | Description         |
|------|---------------------|
| 21   | Bold Off            |
| 22   | Normal intensity    |
| 23   | Italic Off          |
| 24   | Underline Off       |
| 25   | Blink Off           |
| 27   | Inverse Off         |
| 28   | Reveal (Hidden Off) |
| 29   | Strikethrough Off   |

## Text Colors

### Basic Colors
| Color            | Foreground | Background |
|------------------|------------|------------|
| Black            | 30         | 40         |
| Red              | 31         | 41         |
| Green            | 32         | 42         |
| Yellow           | 33         | 43         |
| Blue             | 34         | 44         |
| Magenta          | 35         | 45         |
| Cyan             | 36         | 46         |
| White            | 37         | 47         |
| Default          | 39         | 49         |

### Bright Text Colors (High-Intensity)
| Bright Color     | Foreground | Background |
|------------------|------------|------------|
| Bright Black     | 90         | 100        |
| Bright Red       | 91         | 101        |
| Bright Green     | 92         | 102        |
| Bright Yellow    | 93         | 103        |
| Bright Blue      | 94         | 104        |
| Bright Magenta   | 95         | 105        |
| Bright Cyan      | 96         | 106        |
| Bright White     | 97         | 107        |

## 256-Color Mode
To use 256 colors:
```
\033[38;5;<n>m  // Foreground color
\033[48;5;<n>m  // Background color
```

- Replace `<n>` with a number between 0 and 255.

## RGB Colors (24-bit True Color)
For True Color, specify RGB values:

```
\033[38;2;<r>;<g>;<b>m  // Foreground RGB
\033[48;2;<r>;<g>;<b>m  // Background RGB
```

- Replace `<r>`, `<g>`, `<b>` with values between 0–255.

## Cursor Movement

| Code               | Description                      |
|--------------------|----------------------------------|
| \033[nA           | Move cursor up by n lines        |
| \033[nB           | Move cursor down by n lines      |
| \033[nC           | Move cursor forward by n chars   |
| \033[nD           | Move cursor backward by n chars  |
| \033[nE           | Move cursor to start of n lines down |
| \033[nF           | Move cursor to start of n lines up   |
| \033[nG           | Move cursor to column n          |
| \033[n;nH         | Move cursor to row n, column n   |
| \033[s            | Save cursor position             |
| \033[u            | Restore saved cursor position    |

## Screen & Text Manipulation

| Code               | Description                      |
|--------------------|----------------------------------|
| \033[2J          | Clear entire screen              |
| \033[1J          | Clear from cursor to beginning   |
| \033[0J          | Clear from cursor to end         |
| \033[2K          | Clear entire line                |
| \033[1K          | Clear from cursor to start of line |
| \033[0K          | Clear from cursor to end of line |
| \033[?25l        | Hide cursor                      |
| \033[?25h        | Show cursor                      |

---

This should cover everything about ANSI Escape Codes
