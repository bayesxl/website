Built upon Hyde, a brazen two-column [Jekyll](http://jekyllrb.com) theme that pairs a prominent sidebar with uncomplicated content. It's based on [Poole](http://getpoole.com), the Jekyll butler.

# Instructions for upkeep

## Adding papers

1. Add pdf to bayesxl/website/public/pdfs as \[first author\]\[year\]\[first word of title\].pdf

2. Add bibtex entry to bayesxl/website/_bibliography/\[ConfJour | Preprints | Workshop | Theses\]_bib.bib 

The following format is for a conference:

@inproceedings{\[first author\]\[year\]\[first word of title\],

title = {},

url = {},

abstract = {The whole thing},

language = {en},

urldate = {},

booktitle = {Conference Name},

author = {Lastname, Firstname and Lastname, Firstname and Lastname, Firstname and ...},

year = {},

note = {Link to github code, if there is code},

pages = {},

file = {\[first author\]\[year\]\[first word of title\].pdf}

}

## How to Preview Changes (on a Mac)

If you have another machine, figure it out, and document it here.

  > git clone https://github.com/bayesxl/website.git
  
  > cd website
  
  > brew install ruby
  
  > echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile

Then relaunch terminal.

  > gem install --user-install bundler jekyll
  
  > gem install bundler:1.17.3
  
  > bundle install
  
  > bundle exec jekyll serve
