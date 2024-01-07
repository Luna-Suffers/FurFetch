# FurFetch - E621 Image Downloader
E621 Image Downloader written in Python

## Installation
FurFetch requires no prior downloads/installations; other than a copy of Windows (Does not work on MACOS currently) <br>
Click on releases and select the latest release. Then download FurFetch.zip from that release. <br>
Unzip this in a directory of your choosing and run FurFetch.exe - You may get a windows defender warning simply click 'more info' and then 'run anyway' which will permanently whitelist the file (you won't get the warning again) 

## Setup
The console will display a message that two new files have been created - 'userData.json' and 'userTags.txt' <br>
Firstly open 'userData.json' (which can be opened using notepad) and replace 'YOUR USERNAME HERE' with your E621 Username and 'YOUR API KEY HERE' with you api key that you can get from 'Manage API access' under the accounts tab: <br>

![Manage API Access](https://github.com/Luna-Suffers/FurFetcher/assets/128991823/01af27e7-6843-4f43-9165-24635d57dc88) <br>
Create a new key and past that in 'userData.json' <br>

Now move to 'userTags.txt'; you will see that this already contains some data - feel free to run this to confirm that you have setup 'userData.json' correctly it should download a single image under 'FurFetchDownloads/Kieran_Lockworkorange_2023'

If this all works then congratulations! You have setup FurFetch correctly.

## Tags
On E621 image 'tags' fall under six main categories:
* GENERAL -  tags for 'things' that do not fall under other categories (e.g., female, chair, sitting) <br>
* SPECIES - tags that denote animal species (i.e 'fox', 'horse', etc) <br>
* CHARACTER - tags that link to a specific character name (i.e 'Judy Hopps') <br>
* ARTIST - tags that link to a specifc artist (i.e Luna_Suffers) <br>
* INVALID -  tags that are not allowed on any posts, such as things that are too common and unspecific to individually tag (e.g. face, neck, eyes) or common tagging errors (i.e horsemale rather than horse male)
* LORE - rarely used tags that offer extra context or relevancy to the image (i.e 'Zootopia' would be a lore tag for 'Judy Hopps') <br>
* META - tags that correspond to metadata associated with the image (i.e filetype, size, date of upload) <br>

As well as these tags I have added 'LIMIT' at the bottom of userTags.txt. Whilst this isn't an official 'tag' it is used by FurFetch to determine how many images you wish to download (i.e 5, 50, 200). Leaving it blank defaults to the maximum of 320 photos. 

## Upcoming Features / Known Issues
* Greater detail to error messages; especially when it comes to why tags are rejected
* Partial searching using a mixture of tags (if no posts found with all of them)
* Faster downloading of images
* Not completely replacing userData or userTags files if either is missing (saves you reentering data if the file is still there)
