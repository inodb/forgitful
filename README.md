# Forgitful?
Do you regularly forget to add changes to your git repos while working on an
analysis? This script might be something for you!

## How it works
Forgitful looks for changes in the directory of the specified git repos using
`find`. The result of that find is stored in a tracker inside the repo. Every
time there are changes in the file an email reminder is sent. That's right
forgitful tracks changes in the git directory and all subdirectories.

## Installation
Edit the [configuration file](config.yml) to your likings. Run once to test:
```
bash forgitful config.yml
```
Add it to your crontab to run the script on a regular basis:

```sh
crontab -e
```
For my laptop for instance I run the script on every reboot by adding this line
```sh
@reboot bash /Users/username/git/forgitful/forgitful /Users/username/git/forgitful/forgitful/production.yml
```
