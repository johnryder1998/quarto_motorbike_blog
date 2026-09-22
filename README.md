## John's motorbike blog

This repository host the files which make John's motorbike blog website.

The website currently resides on a free domain:

https://quarto-motorbike-blog.johnryderwhiting.workers.dev/


Local rendering procedure

```bash
$ git branch

$ quarto render

$ git add .

$ git commit -m "$(date)"

$ git push origin [main|internet_published]

# check all links are valid
$ lychee --threads 1 --max-concurrency 1 --accept 100..=103,200..=299,429 "**/*.qmd"
```
