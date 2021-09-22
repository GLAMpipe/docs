---
title: 'List of nodes'
---

Here are the nodes that are available or planned. Each node will be introduced in a tiny tutorial.

## Import data

### Import from a web API

**FINNA import**  
Import media metadata from FINNA, the search service to Finnish museums, archives and libraries.

**Flickr import**  
Import media metadata from Flickr. Requires an API key.

**Internet Archive import**  
Import data from Internet Archive, based on the advanced query.

**Map Warper import**  
Import map metadata (not images) for all maps in a Map Warper instance.

**Wikidata import** (planned)  
Import data from Wikidata based on a SPARQL query.

**Wikimedia Commons import** (planned)  
Import media metadata from Wikimedia Commons.

### Read files

**Online CSV import**  
Import data from an online CSV file.

**Local CSV import**  
Upload and import a CSV file.

### Local directory

**Recursive directory scan**  
Recursive directory scan. Only works with local files.

### Paste data

**Paste data from the clipboard**  
Paste data from the clipboard (planned)

## Process data

### Fields

**Add a row**  
Add a row of data to a field if a search criteria is met.

**Concatenate fields**  
Concatenate string fields with other strings.

**Combine fields to an array**  
Combine values from fields to an array.

**Count characters**  
Count characters of a field.

**Check if a field has a value**  
Boolean value based on a field value.

**Detect language**  
Detect language of a field. Please note that detection is not reliable for short texts.

**Regexp extract**  
Extract a string based on a regular expression.

**Search and Replace**  
Search and replace a string. You can use regular expressions.

**Split**  
Split field to an array.

**Substring**  
Extract a string between two strings.

**URL to field**  
Fetch textual content from a URL to a field.

### Wikimedia templates

**Institution template**  
Format data for Wikimedia Commons Institution template.

**Other date template**  
Format dates for Wikimedia Commons Other date template.

**Creator template**  
Format data for Wikimedia Commons Creator template.

**Create Wikimedia Commons metadata template**  
Format data for Wikimedia Commons metadata templates.

### Files & documents

**Create file checksums (SHA1, MD5)**  
Calculate checksums for files. Only works for local files.

**Check if a file is in Wikimedia Commons**  
Checks if file is already in Wikimedia Commons, using SHA1-checksum. First create checksums with the Create file checksums node.

### Lookups

**URL checker**  
Make a HEAD request to an URL and save the response code.

**Match Wikidata** (planned)  
Reconcile the value of a field to items in Wikidata.

**Wikidata lookup** (planned)  
Find values based on matches in Wikidata. You must first match Wikidata items using the Match Wikidata node.

## Get files

**Download files**  
Download a file from a URL.

**Download Flickr images**  
Download any image size from Flickr. First use the Flickr getSizes node.

## Export files and data

### Save data locally

**CSV export**  
Export a GLAMpipe collection as a CSV file. Exports arrays but does not export objects.

### Upload data and files to web

**Upload to Wikimedia Commons**  
Upload files and metadata to Wikimedia Commons.

**Export to Wikidata** (planned)  
Upload data to Wikidata.

### Export to a GLAMpipe collection

**Group records by field value**  
Group records based on values in a field.

