# PolMeth XXXVII website

This is the code for the official website for the 2020 Annual Conference of the Society for Political Methodology (University of Toronto, July 16-18, 2020).  The website is based on similar initiatives from the field of computer science, and is a stripped down version forked from the [official ACL 2020 website repository](https://github.com/acl-org/acl-2020).

Just like ACL2020 and NAACL 2019, this repo is currently using the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/).

# Forking this repository for a new conference

This PolMeth XXXVII website can be forked to be used in future years (or other conferences).  It is designed for GitHub Pages hosting.

## Steps
 
1. Make sure that Ruby and RubyGems are installed on your machine for local development.

2. Install the jekyll and bundler gems: `gem install jekyll bundler`

3. Clone this repository, and make changes as appropriate.

4. Start the jekyll server by running `bundle exec jekyll serve`.

5. You can then see the website at http://localhost:4000.

## Important Files

If you fork this repository, the following files are the ones to pay attention to in order to create content for the website:

- `_pages/xxx.md` : The markdown files contain the main contents of the different web pages of the website. Please note that
  once you fork, you would need to move the already existing .md files out into a different folder so that old pages do not
  get rendered into the new website.

- `downloads/` : Contains files that can be downloaded from the website.

- `_sass/minimal-mistakes/*.scss` : SASS files that control the look and the feel of the website. The file `_program.scss` is not part of the them and controls the look and feel of the web schedule page.

- `_data/navigation.xml` : YAML file that contains the links in the masthead at the top of the website and also links in the various sidebars. 

- `_config.yml` : YAML file that contains meta-information about the website that should be set properly for a new conference. Details are given in the comments in the file. You must edit this file properly before making the website public.

- `CNAME` : You should delete this file since this contains the old external domain from the older conference. This file will be
  automatically re-generated when you add the new external domain for the new conference. If you do not remove this file, you will
  get a page build warning from GitHub.

## Domain Setup

The following settings connect the the main domain booked for the conference (e.g. `naacl2019.org`) with the underlying Github Pages build. 

On the domain side, the following DNS settings need to be set up: all four IPs belong to Github, the last row connects the www subdomain to the main domain:

```
A   @   185.199.108.153 
A   @   185.199.109.153 
A   @   185.199.110.153 
A   @   185.199.111.153 
CNAME www   naacl2019.org
```

In the settings for the repository on GitHub, the "custom domain" needs to be set to the main domain (e.g., `naacl2019.org`). This will create a CNAME file in the top folder of the Github repository. Note that it may take a few minutes for the changes to become effective until they are propagated through the DNS servers.

# License

The MIT License (MIT)

Copyright (c) 2019 Society for Political Methodology.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
