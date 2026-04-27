# pdf-metadata-stripper

A very robust, fully POSIX-compliant shell script to sanitize PDF files by stripping all metadata and linearizing the internal structure for optimized web viewing.

## Features

- **Metadata Stripping:** Removes all tags (Author, Software, GPS, etc.) using `exiftool`.
- **Structural Cleanup:** Rebuilds the PDF and removes incremental updates/history using `qpdf`.
- **Web Optimization:** Linearizes the PDF for "Fast Web View" (streamable PDFs).
- **Safety First:** Handles filenames with spaces, dashes, and special characters.
- **Timestamp Preservation:** Restores the original file modification time after processing.
- **Dependency Check:** Reports all missing packages at once for easier installation.

## Installation

1. **Install requirements:**
   On Debian/Ubuntu-based systems (including Debian, Ubuntu, Linux Mint, LMDE, etc.), run:
   ```bash
   sudo apt-get update && sudo apt-get install qpdf libimage-exiftool-perl
   ```

2. **Make the script executable:**
   ```bash
   chmod +x pdf-metadata-stripper
   ```

## Usage
   The script is flexible and can be used in two ways:

1. **Automatic Batch Processing**

   If no arguments are provided, it automatically processes all `.pdf` files in the current directory:
   ```bash
   ./pdf-metadata-stripper
   ```

2. **Specific Files or Paths**
   ```bash
   ./pdf-metadata-stripper report.pdf /home/user/documents/audit.pdf
   ```

## Why use this?

When you create a PDF, it often contains hidden information about your system, software versions, and edit history. This script ensures your documents are:

1. Private: All metadata and incremental history are wiped.

2. Professional: Files are optimized for web viewing (linearized).

3. Consistent: The original file modification timestamps are preserved on the filesystem.

## License

This project is licensed under the MIT License - see the header of the script for details.

## Author

Vlastimil Burián, info@vlastimilburian.cz
