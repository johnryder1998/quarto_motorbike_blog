## John's motorbike blog

This repository host the files which make John's motorbike blog. The website currently resides on the following free domain:

https://quarto-motorbike-blog.johnryderwhiting.workers.dev/

The `working_branch` is where the under construction unpublished site is stored. The `internet_published` branch stores the internet published site. Recall, both branches are visible to the internet.

Push local changes to remote `working_branch`.
```bash
$ git switch working_branch

# remove all metadata from images
$ exiftool -verbose -all= -overwrite_original -ext jpg -ext JPG -ext jpeg -ext JPEG -ext png /home/whitingj/quarto_motorbike_blog/images/

# check all links are valid
$ lychee --threads 1 --max-concurrency 1 --accept 100..=103,200..=299,429 "**/*.qmd"

# preview site locally
$ quarto preview

# render site
$ quarto render

$ git add .

$ git commit -m "$(date)"

$ git push origin working_branch
```

If happy with how `working_branch` looks, merge `working_branch` into `internet_published` branch for the changes to go live on website.

