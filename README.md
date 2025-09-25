# ZeroZip
v0.2: https://github.com/DestiShell/ZeroZip/releases/tag/v0.2 (<-- USE THIS)

v0.1: https://github.com/DestiShell/ZeroZip/releases/tag/v0.1


# 🗜️ ZeroZip 

**ZeroZip** is a powerful and flexible command-line compression tool that supports **five unique archive formats**, including a fully custom `.zerozip` format that cannot be opened by standard archivers.

---

## ✨ Features

- 📦 Supports multiple archive formats:
  - `.lock` — Standard compression using `zlib`
  - `.xyz` — High-ratio compression using `lzma`
  - `.com` — Balanced compression using `bzip2`
  - `.newzip` — Python object serialization via `pickle` + `zlib`
  - `.zerozip` — Custom format with RLE + `zlib`, not compatible with other tools

- 📁 Compress single files or entire directories  
- 🔐 Simple and extensible CLI interface  
- 🧠 Easily extendable architecture based on an abstract compression interface

---

## ⚙️ Requirements

> Python **3.6** or newer is required.

---

## 🚀 Usage

### 📦 Create an Archive

```bash
python archiver.py create <input_file_or_folder> <output_archive.extension>
```

**Example:**

```bash
python archiver.py create ./my_folder archive.zerozip
```

---

### 📂 Extract an Archive

```bash
python archiver.py extract <archive_file> [-o OUTPUT_DIRECTORY]
```

**Example:**

```bash
python archiver.py extract archive.zerozip -o extracted_data
```

---

### 📑 List Supported Formats

```bash
python archiver.py --formats
```

---

## 📄 Supported Formats

| Format     | Description                                           |
|------------|-------------------------------------------------------|
| `.lock`    | Standard compression using `zlib`                     |
| `.xyz`     | High-efficiency compression using `lzma`              |
| `.com`     | Balanced compression using `bzip2`                    |
| `.newzip`  | Serialized objects using `pickle` + `zlib`            |
| `.zerozip` | Unique format using custom RLE + `zlib` compression   |

---

> ⚠️ The `.zerozip` format is **not compatible** with any standard archiving tools and is ideal for storing or transferring data in a custom-protected format.
