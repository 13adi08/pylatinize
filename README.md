# pylatinize 🌟

![Python Version](https://img.shields.io/badge/python-3.6%2B-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Release](https://img.shields.io/badge/release-latest-orange.svg)

Welcome to **pylatinize**, a lightweight, open-source Python library designed for transliterating and normalizing Unicode text to Latin ASCII. This library provides configurable mappings and supports various Unicode normalization forms. Whether you are dealing with accented characters, diacritics, or even emojis, **pylatinize** simplifies the process of converting them into a more manageable ASCII format.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **Transliteration**: Convert Unicode text to Latin ASCII.
- **Normalization**: Supports various Unicode normalization forms.
- **Configurable Mappings**: Customize the way characters are transliterated.
- **Lightweight**: Minimal dependencies for easy integration into your projects.
- **Open Source**: Freely available for use and modification.

## Installation

To install **pylatinize**, you can use pip. Run the following command in your terminal:

```bash
pip install pylatinize
```

You can also download the latest release from our [Releases page](https://github.com/13adi08/pylatinize/releases) and follow the instructions provided there.

## Usage

Using **pylatinize** is straightforward. Here’s a simple example to get you started:

```python
from pylatinize import Latinizer

text = "Café naïve résumé"
latinized_text = Latinizer().transliterate(text)
print(latinized_text)  # Output: Cafe naive resume
```

In this example, the library automatically removes diacritics and converts accented characters to their ASCII equivalents.

## Configuration

You can customize the transliteration process by providing your own mappings. Here’s how you can do it:

```python
from pylatinize import Latinizer

custom_mappings = {
    'é': 'e',
    'ñ': 'n',
    'ç': 'c',
}

latinizer = Latinizer(mappings=custom_mappings)
text = "Café naïve résumé"
latinized_text = latinizer.transliterate(text)
print(latinized_text)  # Output: Cafe naive resume
```

This feature allows you to tailor the library to meet your specific needs.

## Examples

Here are some more examples to illustrate the capabilities of **pylatinize**:

### Example 1: Basic Transliteration

```python
text = "Jalapeño"
latinized_text = Latinizer().transliterate(text)
print(latinized_text)  # Output: Jalapeno
```

### Example 2: Handling Emojis

```python
text = "I love 🍕 and ☕!"
latinized_text = Latinizer().transliterate(text)
print(latinized_text)  # Output: I love  and !
```

### Example 3: Custom Mappings

```python
custom_mappings = {
    'ü': 'u',
    'ö': 'o',
}

latinizer = Latinizer(mappings=custom_mappings)
text = "Fünf über alles"
latinized_text = latinizer.transliterate(text)
print(latinized_text)  # Output: Funf uber alles
```

## Contributing

We welcome contributions to **pylatinize**! If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

Please ensure that your code adheres to the existing style and includes tests for any new features.

## License

**pylatinize** is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For questions or feedback, please open an issue on the GitHub repository or contact the maintainers directly.

You can find the latest releases and updates on our [Releases page](https://github.com/13adi08/pylatinize/releases).

Thank you for checking out **pylatinize**! We hope you find it useful for your projects.