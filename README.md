# Eleven Creative site

http://stackoverflow.com/questions/18304025/bulk-renaming-of-files-in-powershell-with-sequential-numeric-suffixes

$i = 0
Get-ChildItem *.jpg | %{Rename-Item $_ -NewName ("$($i).jpg" -f $i++)}

## Workflow
1. Create collection table with id, name, and description
2. Save base64-encoded images to collection
	1. Pick collection from dropdown
	2. Select "preview" image
		1. Preview image might need to be saved to some sort of "showcase" collection used for displaying images on home page
	3. Load images
	4. Assign collection id to images
3. Create endpoint which gets images for a given collection [Route("*/collection/{id}*")]


## TODO
- [ ] Create *collections* table
- [ ] Create _showcase_ collection (used to display images on homepage
- [ ] Create page for loading images
	1. Name the collection
	2. Select the showcase image
	3. Upload the images
	4. Store the images in SQL
- [ ] Load the _showcase_ collection on page load
- [ ] On click of _showcase_ collection image, retrieve collection thumbnails for that collection
- [ ] On click of image, load full-sized image
