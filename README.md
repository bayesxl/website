Built upon Hyde, a brazen two-column [Jekyll](http://jekyllrb.com) theme that pairs a prominent sidebar with uncomplicated content. It's based on [Poole](http://getpoole.com), the Jekyll butler.

# Instructions for upkeep

## Adding papers

1. Add pdf to bayesxl/website/public/pdfs as \[first author\]\[year\]\[first word of title\].pdf

2. Add bibtex entry to bayesxl/website/_bibliography/\[ConfJour | Preprints | Workshop | Theses\]_bib.bib 

The following format is for a conference:

    @inproceedings{[first author][year][first word of title],
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
        file = {[first author][year][first word of title].pdf}
    }

3. Consider changing your sample paper (see below)

## Adding Yourself

Add a picture of yourself to bayesxl/website/public/image

Go to bayesxl/website/people.md.

Add an entry under Current Members. Mike goes on top, then the later-to-graduate students go above the sooner-to-graduate students.

Format: (the curly braces are not part of the markdown syntax)

    <img src="../public/image/{filename}" width="200">

    [**{Your Name}**]({link to personal website})

    [Google Scholar]({link to your Google Scholar page})

    Sample paper : [{Paper Title}]({link to paper})

    Here through : {Expected Graduation Date}

    Favourite prior : {Your Favorite Prior Distribution}

    Favourite {“terrain” | “cloud type” | “insectivore” | “racquet sport” | “quaint slang” | “kind of boat” | “celebrity hairstyle” | “capital city” | “seaside town” | “regular polyhedron” | “vitamin” | “noble gas” | “ancient ruin” | “tree” | “protein source” | “debunked scientific theory” | “scent” | “function f : R -> R” | “species in lepidoptera” | “frequency” | “curated collection of objects” | “pickled vegetable”} : {Your Favorite of That Thing; e.g. archipelago, bullocks, sycamore, rain, or yearly. “But Michael,” you say, “I don’t have a cached favorite of any of those things. Can’t I do a favorite movie or ice cream flavor?” No. Try harder.}
    
Having "../" at the front of the filepath to the image is wrong for viewing the image on github, but right for the website. To check the image on github, change it to "./", and click Preview Changes. (But then switch it back to "../" before committing the change.)
    
## How to Preview Changes (on a Mac)

If you have another machine, figure it out, and document it here.

      git clone https://github.com/bayesxl/website.git
      cd website
      brew install ruby
      echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile

Then relaunch terminal.

      gem install --user-install bundler jekyll
      gem install bundler:1.17.3
      bundle install
      bundle exec jekyll serve
