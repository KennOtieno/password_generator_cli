# Password Generator CLI

A CLI password generator built with Go

## Installation

```bash
git clone https://github.com/KennOtieno/password_generator_cli.git
cd password_generator_cli
```

### Build the Application

**On Linux/Mac:**
```bash
make build
```

**On Windows (PowerShell/CMD):**
```powershell
go build -o bin/passgen.exe
```

**On Windows (Git Bash/WSL):**
```bash
go build -o bin/passgen
```

## Usage

**On Linux/Mac:**
```bash
make run ARGS="[flags]"
# or
./bin/passgen [flags]
```

**On Windows (PowerShell/CMD):**
```powershell
./bin/passgen.exe [flags]
```

**On Windows (Git Bash/WSL):**
```bash
./bin/passgen [flags]
```

## Flags

* `-l --length int`: Length of the password (default: 15)
* `-c --count int`: Number of passwords to generate
* `-L --lowercase bool`: Include lowercase characters
* `-U --uppercase bool`: Include uppercase characters
* `-n --numbers bool`: Include numeric values
* `-cp --copy bool`: Copy to clipboard
* `-s --special bool`: Include special characters

## Examples

**Linux/Mac (with make):**
```bash
make run ARGS="-l 14 -U -L -n -s -c 2"
```

**Windows (PowerShell/CMD):**
```powershell
./bin/passgen.exe -l 14 -U -L -n -s -c 2
```

**Direct execution (all platforms):**
```bash
./bin/passgen -l 14 -U -L -n -s -c 2
```

This command generates 2 passwords, each 14 characters long, including uppercase, lowercase, numbers, and special characters.

### More Examples

**Generate a strong 20-character password:**
```powershell
./bin/passgen.exe -l 20 -U -L -n -s
```

**Generate 5 passwords and copy to clipboard:**
```powershell
./bin/passgen.exe -U -L -n -s -c 5 -cp
```

**Generate uppercase and numbers only:**
```powershell
./bin/passgen.exe -l 12 -U -n
```

## Features

* Generate strong passwords
* Use flags to select attributes of your password
* Generate multiple passwords at once
* Copy generated passwords to clipboard
* Option to exclude similar looking passwords
* Save generated passwords to file
* Password strength meter

## Requirements

* Go 1.16 or higher
* Make (optional, for Linux/Mac users)

## Troubleshooting

**Windows users:** If `make` is not recognized, use the direct Go commands shown in the installation section above.

**Permission denied:** On Linux/Mac, you may need to make the binary executable:
```bash
chmod +x bin/passgen
```
