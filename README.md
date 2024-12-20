# thermchem-fw.github.io
Website for the ThermChem-FW fusion SciDAC project, led by Jaime Marian, UCLA

## Core tools

This website uses [Jekyll](https://jekyllrb.com/) and the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme and is hosted on [GitHub Pages](https://pages.github.com/) at <https://thermchem-fw.github.io/>. It uses a number of Jekyll plugins, but one of the most complex of which is [jekyll-scholar](https://github.com/inukshuk/jekyll-scholar), which handles bibliographies based on BibTeX files.

## Contributing

If you're familiar with Jekyll and the GitHub pull request process, feel free to propose your own changes in the form of a pull request. (Please make sure to test your changes with a local Jekyll installation before submitting the pull request.) Otherwise, you're probably best off submitting an issue to the GitHub repository, or reaching out to the point of contact to discuss your needs.

## Adding bibliography entries

The [project bibliography](https://thermchem-fw.github.io/publications/) includes papers, presentations, and other documents that the team wants the community to know about and have access to. To add a new item to the project bibliography, follow these steps in your own fork of the repository and submit a pull request:

1) Add the BibTeX entry to the appropriate file in the [`_bibliography`](https://github.com/ThermChem-FW/thermchem-fw.github.io/tree/main/_bibliography) directory.  See notes below for details of which types of documents are appropriate for each category of publication.
2) *If* you want to host a local PDF copy of the document, add it to the [`assets/documents/`](https://github.com/ThermChem-FW/thermchem-fw.github.io/tree/main/assets/documents) directory using a filename that matches the key in the BibTeX entry. Note that DOIs and reliable externally hosted URLs are preferred to local hosting. See notes below for futher details.

Alternatively, you can send the BibTeX entry and (if appropriate) a file to host locally to the website point of contact.  If you're not familiar with BibTeX, please provide complete bibliographic information and a copy of the file, if appropriate, to the website point of contact.

### Best practices and caveats for bibliography entries

* Ensure that your item is added to the correct `.bib` file so that it will appear in the correct portion of the Publications page.
    * The *Publications* category (`publications.bib`) includes peer-reviewed papers, publicly-posted preprints, technical reports, and similar kinds of documents.
    * The *Presentations* category (`presentations.bib`) includes talks, posters, and similar kinds of documents.
    * The *Other Documents* category (`other.bib`) includes non-peer-reviewed and informal documents that we want to share with the community, for example, the project proposal, annual reports to sponsors, blog posts, etc.
* Try to provide as complete and high quality information as you can, using the existing entries as models.
    * For presentations, use the `@misc` entry type, with details of the presentation venue in the `howpublished` field.
* There are three ways to link to a document:
    * For documents with a DOI, you should use the BibTeX `doi` field to capture the information.  The DOI is always the preferred identifier. Note that the DOI starts with `10.`.  The `https://doi.org/` or `http://dx.doi.org/` prefixes used to turn them into functional URLs are, technically, *not* part of the DOI.
    * For documents hosted at a reliable external URL, you should use the BibTeX `url` field to capture the full URL.
    * Lacking a DOI or reliable external URL, we can host PDF documents locally (i.e., on our website).  In this case, the URL for the documents should *not* appear in the BibTeX entry.  Instead the `jekyll-scholar` plugin is configured to look for a file in the `assets/documents/` directory that matches the key of the BibTeX entry, with a `.pdf` extension and associate it with the displayed reference.
        * Only PDF documents can be hosted locally.
        * The name of the locally hosted file must match the key in the BibTeX entry (except for the `.pdf` extension).
* If your BibTeX entry includes and `abstract` field, the contents will be available with the displayed reference using the HTML `<details>` mechanism.  By default, only the heading ("Abstract") is displayed, but clicking will open the content.

## Point of contact

David Bernholdt (@bernhold) is the primary point of contact for the <https://thermchem-fw.github.io/> website.