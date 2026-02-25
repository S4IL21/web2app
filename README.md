# web2app - modified by S4IL

PyPI package for converting a website **or local HTML file** into a Windows desktop app.

---

## Installation

Install from pip:

```bash
pip install web2app
```

---

## Usage

### Convert a Website

Turn a website into an app:

```python
from web2app import Web2Exe

exe = Web2Exe("https://www.google.com/")
exe.create(output_dir="output")
```

The app name is inferred from the page `<title>`, and the favicon is used as the icon.

---

### Convert a Local HTML File

You can also package a local HTML file:

```python
from web2app import Web2Exe

exe = Web2Exe("index.html")
exe.create(output_dir="output")
```

Local files are automatically converted to a `file:///` URI and loaded into the app.

---

### Custom Name and Icon

You can specify a custom name and icon:

```python
exe = Web2Exe(
    url="https://www.google.com/",
    name="Google",
    icon="assets/logo512.png",
)

exe.create(output_dir="output")
```

The `icon` parameter accepts:

* A file path
* A `PIL.Image` object
* A `BytesIO` object containing image data

## Made it so you can also use local HTML files – S4IL
