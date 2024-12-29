# plh (Polars Help)

A command-line tool to quickly access Polars documentation from your terminal.

## Features

- Quick access to Polars documentation directly from the command line
- Support for all Polars objects and methods
- Easy to navigate class methods and function descriptions
- Works with both DataFrame and LazyFrame operations

## Prerequisites

- Python 3.x
- Required packages (install via `pip install -r requirements.txt`):
  - Polars
  - Rich (for syntax highlighting and beautiful output)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/plh.git
cd plh
```

2. Make the script executable:
```bash
chmod +x plh
```

3. Create a symbolic link to make the command available system-wide:
```bash
ln -s "$(pwd)/plh" ~/bin/plh
```

Note: Make sure `~/bin` is in your PATH. If not, add the following line to your `~/.bashrc` or `~/.zshrc`:
```bash
export PATH="$HOME/bin:$PATH"
```

## Usage

```bash
# Show help for DataFrame methods
plh DataFrame.filter
plh DataFrame.group_by

# Show help for LazyFrame methods
plh LazyFrame.collect

# Show help for functions
plh col
plh lit

# List available methods for an object
plh DataFrame
plh LazyFrame
```

## Examples

```bash
# Get help for filtering operations
$ plh DataFrame.filter
Help for polars.DataFrame.filter:
----------------------------------------
Filter the DataFrame based on a predicate expression.
...

# List all available DataFrame methods
$ plh DataFrame
Module: DataFrame
Available attributes:
- filter
- select
- group_by
...
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
