# Code Line Counter
## Author: Claude 3.7 Sonnet, Kyle Rose
## Version 1.0.0

Small program to walk through a directory structure and count the number of lines in each code file.
Excluded files patterns and directories can be specified in the two CSV files: 'excluded_directories.csv' and 'excluded_extensions.csv'

## Usage:
    python code_line_counter.py [-h] [--verbose] [--output OUTPUT] 
                               [--exclude PATTERN [PATTERN ...]] 
                               [--exclude-dir DIR [DIR ...]]
                               [directory]

## Arguments:
    directory           Directory to analyze (default: current directory)

## Options:
    -h, --help          Show this help message and exit
    --verbose, -v       Show detailed progress while counting
    --output, -o        Output file path to save results (default: print to console)
    --exclude, -e       Additional file patterns to exclude (e.g., '*.lock' '*.toml')
    --exclude-dir, -d   Directories to exclude (e.g., 'venv' '.git')

## Example Usage:
```bash
    python code_line_counter.py /path/to/project --verbose --exclude-dir venv .github node_modules
```