---

category: Notes
type: 'Notes'
url_path: '/dev_notes_jekyll'
title: 'Dev Notes - Jekyll'

layout: null
---

# Jekyll
### Documentation for this website's template:
> [Carte Documentation](https://github.com/Wiredcraft/carte)

### Running jekyll on your localhost:

> `bundle exec jekyll serve`

### Building this documentation and upload to Github pages:

> `bundle exec jekyll build --destination docs/`

### Updating Gem Files
Gem files in Jekyll are similar to Python packages, sometimes there are security issues that needs to be updated.
For example, recently I had to update addressable from 2.7.0 to 2.8.0 in order to avoid security issues.
If Ruby starts to complain about this:

```
Could not find addressable-2.8.0 in any of the sources
Run `bundle install` to install missing gems.
```

Then simply run: `bundle install`


### Controlling the order of sections
Currently, it is a dirty trick, but it works. I cannot get jekyll to work with a single number, so I am using date.
In **_posts**, the date with most recent pops up to the top. For example, **2021_06_30** appears on the top of **2021_06_01**.
It ain't perfect, but it solves our problem.