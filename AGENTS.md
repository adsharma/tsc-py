# Qwen Code Preferences and Setup Instructions

## Python Environment Management

For this project, we prefer using `uv` for managing Python dependencies as it's faster and more reliable than pip in certain environments.

### Installing Development Dependencies

Instead of using pip directly, use uv:

```bash
# Install development dependencies
uv pip install -e .[dev]

# Or if working in a virtual environment:
source .venv/bin/activate
uv pip install -e .[dev]
```

### Running Tests

Use the virtual environment's pytest:

```bash
source .venv/bin/activate
python -m pytest tests/ -v
```

## Project Structure

The project implements a PEG parser for TypeSpec grammar based on the official grammar specification. Key components:

1. `typespec_parser/peg/parser.py` - Custom PEG parser implementation
2. `typespec_parser/parser.py` - Main parser that generates Python dataclasses
3. `example.tsp` and `example.py` - Example TypeSpec content and usage
