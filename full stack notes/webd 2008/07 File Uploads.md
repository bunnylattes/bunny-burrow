---
class: webd 2008
module: module three
date: 2022-02-09
tags: webd-2008, web-development, php, pdo, term-2
---

# File Uploads

### Upload No Filter
- Cannot specify the file type with this code
- enctype="multipart/form-data"
	- encoding type = required to make sure the dialogue box works when the user clicks on the button
- **Files Superglobal:**  $ _ FILES
- else statement: we need to take the file from the temporary database and put it somewhere
	- basename function gives us the name of the file
	- dirname returns the actual direction where the current file exists in
	- DIRECTORY_SEPARATOR is a global file on apache, whatever the OS uses is what this will return
	- append on the file name we got from the basename function
- if statement: check if it worked
	- if there is an error, there will be an error
	- move_uploaded_file(file you want to move, where you want to move it to)
		- ``` move_uploaded_file($_FILES['uploaded_file']['tmp_name'], $newname) ```

**We must check and make sure it's an image or the proper file type to avoid malicious uploads.**

### Upload And Filter

***ENDED AT 11:28, RESTART THERE***

