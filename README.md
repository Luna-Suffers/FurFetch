# FurFetch - E621 Image Downloader
E621 Image Downloader written in Python
![FurFetch](https://github.com/Luna-Suffers/FurFetch/assets/128991823/cc6ab777-fa03-49e8-b7c6-4daf4555ac55) <br>

## New Features
Current Version: 1.2
<ul>
  <li>More Downloading Statistics - Download Rate, Estimated Time Remaining, Photo Number</li>
  <li>More Detailed Error Messages - Check Error Fixes below</li>
  <li><i>Slightly</i> Faster Download Speeds - Changed how requests are handled</li>
  <li>App Consistency - Can run from scratch without closing terminal</li>
</ul>

## Upcoming Features
* Partial searching using a mixture of tags (if no posts found with all of them)
* Faster downloading of images

## Why?
Why did I make an E621 downloader you ask? Well there are many reasons, but mainly I used to use the E621 Downloader by McSib but found it required lots of prerequisite downloads and setup; which is quite lengthy for the common user, so I decided to make my own which could then be compiled to a single app EXE

# Installation
FurFetch requires no prior packages/installations; other than a copy of Windows (Does not work on MACOS or Linux currently) <br>
Click on releases and select the latest release. Then download FurFetch.zip or FurFetch.exe from that release. <br>
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

As well as these tags I have added 'LIMIT' at the bottom of userTags.txt. Whilst this isn't an official 'tag' it is used by FurFetch to determine how many images you wish to download (i.e 5, 50, 200). Leaving it blank defaults to the maximum of 320 photos. <br>

## Error Fixes
You may encounter several errors as the code runs - these messages aim to be as clear as possible but I have included some common fixes below in case it doesnt work: <br>

<b>Error with JSON file please delete and try again</b> - There is an issue with your account name or API key; this may be because you have entered it correctly OR it is an issue with the file itself. Either delete the file and readd your details, or attempt to fix it <br>

<b>Please check details are correct in the userData.json file"</b> - Similar to above, but unlikely to be caused by incorrect entering of details - check your API key is still in date <br>

<b>Webm file detected, skipping...</b> - this is not an 'error' message in the sense, but essentially there are webm (web video) files found under these tags. This code does not install them as it would take too long and cause an issue on both ends of the connection - it is advised to download these yourself from directly from the website <br>

<b>Other Errors</b> - Hopefully most other error messages you recieve are self explanatory (i.e Failed to download Image). Any other errors you recieve may be as a result of the 'request' to the E621 servers. This could be caused by your wifi connection / proxy settings OR caused because of my code (although this is unlikely if the build is up to date). If it is not fixable by you please open an Issue with all the relevant information (platform, supplied tags, wifi connection type)<br>

