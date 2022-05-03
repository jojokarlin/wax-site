---
layout: exhibit
title: 'Exhibit A: Inline Parallax Image'
author: Jojo Karlin
permalink: /exhibits/a/
---

Oh to understand how these images will appear! I worked my way through the template as I revisit all the drawings from the semster.

I was concerned that these essays will be impoverished because of the long swathes of time that stretched between windows on my computer trying to reconcile filenames and image compressions and directories on directories.

Ideally, the liquid includes functions work seamlessly. In practice, you sometimes miss some things.


{% include parallax_image.html collection='sketches' pid='img30' y='50%' %}


I've gone through the passages laid out in the wax template. I've replaced pids with my own pids. I changed those at one point when I realized I was being too descriptive with my pids. Hopefully the file naming will help me keep track. I probably should have stuck to the class drawings only, but I wanted to see how much time it would take to build up a collection. 

My basic process is this:
- I scan the image with my lightweight canon scanner.
- I open the image in Adobe Photoshop, rotate it if needed, and trim the edges. 
- I "Save As" in the website directory with the following filename convention. YYYYMMDD-EventTitle.jpg. I use Adobe to convert to .jpg from the .tif scan.
- I then run the images through imagecompressor.com.
- I unzip the image files in the 'sketches' directory in my wax_site directory.
- I check that my Google sheet has all the pids that correspond to the img directory files.

Beyond this process, I had to check that my images were all what they said they were. Then I tried to clean up dates on my spreadsheet only to break the rake tasks by introducing unacceptable punctuation. I went back to strictly numeric dates. I clobbered the files Wax had previously made and started over. 

I ran these tasks:
```
bundle exec rake --tasks
bundle exec rake wax:derivatives:simple sketches
bundle exec rake wax:derivatives:iiif sketches
bundle exec rake wax:pages sketches
bundle exec rake wax:search sketches
```
These seem to have worked!
I spent some more time trying to tidy topics in my spreadsheet (still not finished) and figure out the dropdown that was falling behind the nav items. I learned about z index and I still didn't fix it until I demoted the nav items.

All in all, it's coming along well.