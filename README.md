<h1 align="center">
	🛠️ pipex
</h1>

<p align="center">
	<b><i>Because sometimes one pipe just isn't enough</i></b><br>
</p>

<h3 align="center">
	<a href="#-about">About</a>
	<span> · </span>
	<a href="#-features">Features</a>
	<span> · </span>
	<a href="#-bonus">Bonus</a>
	<span> · </span>
	<a href="#-usage">Usage</a>
</h3>

---

## 💡 About

> _This project is about handling pipes and redirections, just like the shell does._

Pipex is a 42 project that recreates the behavior of shell pipes and redirections in C. It demonstrates deep understanding of process management, file descriptors, pipes, and command execution.

The program mimics the shell command:
```bash
< file1 cmd1 | cmd2 > file2
```

This project introduces students to:
- Process creation and management (fork, execve)
- Inter-process communication (pipes)
- File descriptor manipulation
- Command path resolution and execution

## 🚀 Features

### Mandatory Part
- **Single pipe functionality**: `cmd1 | cmd2`
- **Input/output redirection**: `< input_file` and `> output_file`
- **Command path resolution**: Finds commands in PATH
- **Error handling**: Comprehensive error management
- **Memory management**: Proper allocation and freeing

## 🏆 Bonus - Because Basic is Boring

**🎯 FULL BONUS IMPLEMENTED** - All extra features completed!

### ✨ Enhanced Features:
- **🧩 Multiple Pipes**: Handle unlimited commands like a boss - `cmd1 | cmd2 | cmd3 | ... | cmdn`
- **📝 Here Document**: Support for `<<` delimiter with custom limiters
- **📎 Append Mode**: `>>` redirection that plays nice with existing files
- **🛡️ Robust Error Handling**: Gracefully handles everything that can go wrong (and trust me, a lot can)

### 🎪 Bonus Usage Examples:
```shell
# Pipe party! Multiple commands dancing together
$ ./pipex file1 "cat" "grep gold" "sort" "uniq" "wc -l" result.txt

# Here document magic - like a conversation with your terminal
$ ./pipex here_doc EOF "grep treasure" "sort -r" "head -5" findings.txt

# Append mode - because overwriting is so rude
$ ./pipex log.txt "tail -f" "grep error" "sed 's/error/bug/'" >> all_errors.txt
```

## 🛠️ Usage

### Requirements

The project is written in C and requires:

- **`gcc` compiler**
- **Make**
- **Custom Libft** library (included)

### Instructions

**1. Compiling the project**

To compile the mandatory part:
```shell
$ make
```

To compile the bonus part (recommended - it's cooler):
```shell
$ make bonus
```

**2. Running the program**

Basic usage (mandatory):
```shell
$ ./pipex file1 "cmd1" "cmd2" file2
```

Bonus usage (the fun part):
```shell
$ ./pipex file1 "cmd1" "cmd2" "cmd3" ... "cmdn" file2
```

Here Document usage (bonus):
```shell
$ ./pipex here_doc LIMITER "cmd" "cmd1" file
```

## 🧩 Project Structure

- [`src/`](https://github.com/handyman0/42-pipex/tree/main/src) - Main source files for mandatory part
- [`bonus/`](https://github.com/handyman0/42-pipex/tree/main/bonus) - **Where the magic happens** - Bonus implementation
- [`include/`](https://github.com/handyman0/42-pipex/tree/main/include) - Header files
- [`libft/`](https://github.com/handyman0/42-pipex/tree/main/libft) - Custom Libft library
- [`.vscode/`](https://github.com/handyman0/42-pipex/tree/main/.vscode) - VS Code configuration
- [`Makefile`](https://github.com/handyman0/42-pipex/blob/main/Makefile) - Build configuration

## 📋 Testing

### Manual Testing

Test your pipe skills:
```shell
# Basic test - are you alive?
$ ./pipex input.txt "ls -l" "wc -l" output.txt

# Stress test - how many pipes can you handle?
$ ./pipex big_file.txt "cat" "grep x" "sort" "uniq" "wc -l" final.txt

# Error handling - break it if you can!
$ ./pipex non_existent.txt "invalid_cmd" "wc -l" output.txt
```

---

<p align="center">
	<em>When life gives you pipes, make a pipeline! 🎯</em><br>
	<em>Now with 100% more bonus features! 🎪</em>
</p>

<p align="center">
	<strong>"I pipe, therefore I am" - René Descartes (probably)</strong>
</p>
