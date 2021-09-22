---
title: 'Tutorial 4: Working with files'
visible: true
---

In this tutorial you'll find out how to download files from URLs in your data, how to extract text from PDF files and how to calculate checksums for files.

Here is a small dataset (15 articles) in CSV format:
- [view in Google Drive](https://drive.google.com/file/d/1gGECVgRdVm7oWpFkJv7yKHVwYEl4N-nQ/view)
- [direct download link](https://drive.google.com/uc?export=download&id=1gGECVgRdVm7oWpFkJv7yKHVwYEl4N-nQ&noprocess)

#### Task 1
- Download PDF files from URLs in your data

##### Background information
File download node can be found on **Process data > File operations > Download file**. You must give file path field as input.

#### Task2
- Extract text from PDF. 

##### Background information
There is a text extraction node in **Process data > File operations -> PDF: extract text**. You need to give absolute file path to as in input to the node.

#### Task 1
- Download PDF files from URLs in your data

##### Background information
Checksums are used to check integrity of files. It the case of Wikimedia Commons it can also used to check if certain file is already in commons or not. Checksum node can be found on File operations section.

##### Solution
Create the Checksum node, give the file path field as an input and execute it. 