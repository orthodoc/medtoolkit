## hdr-blog [![Build Status](https://travis-ci.org/orthodoc/medtoolkit.svg?branch=master)](https://travis-ci.org/orthodoc/medtoolkit)

### Getting Started

To use this theme, it's just like using any other Jekyll template:

*Step 1:* [Install Jekyll](https://jekyllrb.com/docs/installation/)

*On windows*
If on windows you will need the ruby devkit available here: [rubyinstaller](http://rubyinstaller.org/).

*Step 2:* Clone this repo to your computer

```bash
git clone git@github.com:checkhealthco/hdr-blog.git
```

*Step 3:* Run `gem install bundler; bundle install` inside the new `/hdr-blog/` folder that was just created to install the required ruby dependencies.

*Step 4:* Run `npm install` to install the skeleton sass and its dependencies.

*Step 5:* Tweak `_config.yml`.

Just fill in everything in the `# Site settings` section.
You'll want to set your site's title, your name, your twitter username, etc.

*Step 6:* Run `rake serve` and then open
[http://localhost:4000/](http://localhost:4000/) to see your site!

*Step 7:* Build the site

- Clean up the folders: `rake clean`
- Build the site: `rake build` Note that this will clean before building the site

*Step 8:* Publish your site
[just like any other Jekyll site](https://jekyllrb.com/docs/deployment-methods/).
Specifically for this project:
- Fill in `s3_website.yml` with production variables related to AWS S3 bucket
- Push the site with: `rake publish`

### Notes:

- Using travis to publish the site on build success

- Use the variables in .sample.env file to fill in the env variables at travis-ci

- Using [Skeleton CSS](http://getskeleton.com/) responsive CSS boilerplate.
  Excluding the optional web fonts, the example page weight is only one 7kB HTML file plus one 9kB CSS file. Multiple CSS files are concatenated together using includes, to minimize page requests. Add your own overrides and some inline SVGs or data URIs for an extremely fast site.

### License

MIT. See LICENSE file in repo.
