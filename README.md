Duplicate File Finder
Finds duplicate files by comparing their actual content, not just names.

What it does

Scans a folder (including subfolders), calculates MD5 hash of each file, and shows which files are identical. Also tells you how much space you're wasting.

Usage

bashpython3 duplicate_finder.py
Enter a path or press Enter for current directory.
Example output
Found 2 sets of duplicates:

Set 1 (3 files, 45,231 bytes each):
  - /Downloads/photo.jpg
  - /Downloads/photo_copy.jpg
  - /Backup/photo.jpg

Total space wasted by duplicates: 90,462 bytes (0 MB)

How it works

Uses hashlib.md5() to generate a hash for each file. Files with same hash = same content. Groups them and shows the results.
Reads files in chunks so it can handle large files without crashing.

Requirements

Python 3.6+ (standard library only)
