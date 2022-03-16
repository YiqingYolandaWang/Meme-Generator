# Meme Genereator

The goal of this project is to build a "meme generator" – a multimedia application to dynamically generate memes, including an image with an overlaid quote.

## Overview

The project mainly use the following two files to generate memes.

- 'meme.py': randomly generate images based on the given path and text from a local csv, docx, pdf or txt files, or by entering text through the command line.

- 'app.py': a web server generates random memes by using local csv, docx, pdf or txt files, or by entering image's url.

## Setting up & Running the Program

In the project root directory, type the following into the terminal to run the program:
- 'python3 app.py'
- 'python3 meme.py'

## Sub-modules

In QuoteEngine directory, sub-modules are:

- 'QuoteModel.py': represent quote's body and author

- 'CSVIngestor.py': parse content from CSV files for memes using the 'pandas' dependency.

- 'DocxIngestor.py': parse content from Docx files for memes using the 'python-docx' dependency.

- 'PDFIngestor.py': parse content from PDF files for memes using the xpdf's 'pdftotext' tool.

- 'TextIngestor.py': parse content from text files for memes.

- 'Ingestor.py': choose ingestor for parsing files.

- 'IngestorInterface.py': The abstract base class, which is the parent class of the following files:
    - 'Ingestor.py'
    - 'CSVIngestor.py'
    - 'DocxIngestor.py'
    - 'PDFIngestor.py'
    - 'TextIngestor.py'

In MemeEngine directory, sub-module is 'MemeEngine.py'. It generates a new meme based on the given image, quote's body and quote's author using the 'Pillow' dependency.
