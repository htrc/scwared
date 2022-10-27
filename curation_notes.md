# SCWAReD Workset Curation and Hosting

## Random sites to explore
- <http://kaggle.com> (hosted datasets and jupyter notebooks)
- Microsoft [Azure Open Datasets](https://azure.microsoft.com/en-us/services/open-datasets/?cdn=disable#overview). Good for examples of how datasets are documented.
- American Chemical Societry: <https://www.cas.org/covid-19-antiviral-compounds-dataset>, example stand-alone data set.
- CORGIS: <https://think.cs.vt.edu/corgis/>, looks like a small-scale departmental teaching site.
- [Registry of Open Data on AWS](https://registry.opendata.aws), [registry files](https://github.com/awslabs/open-data-registry) are hosted on github.
- [21 Places to Find Free Datasets for Data Science Projects](https://www.dataquest.io/blog/free-datasets-for-projects/)
Extended workset format: id, author, title, date?

## Possible directory structure for hosted worksets

```
+ workset title
    + docs
        + index.html
        + introduction.md
        + project_report.md
        + images
    + worksets
    	+ workset.csv
	+ workset.json
	+ README-worksets.md
    + datasets
        + dataset1
            + dataset1.csv
            + README-dataset1.md
        + dataset2
            + dataset2.csv
            + README-dataset2.md
        + dataset3
            + dataset3.json
            + README-dataset3.md
```
See <https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site> for configuring a repository directory to serve pages at github.io.
			
## Next steps
- github account for SCWAReD projects (and other curated worksets)?
- naming conventions for SCWAReD projects (and other curated worksets)? Common prefix, e.g, ws (workset), cws (curated workset)?
- show some of the more interesting examples to team.
- look more at github, including <https://education.github.com> and <https://pages.github.com>.
    - Brief explanation of Github Sites: <https://www.youtube.com/watch?v=2MsN8gpT6jY>
    - Interesting examples using Github sites: 
        - <http://mbtaviz.github.io/> (and its source code: <https://github.com/mbtaviz/mbtaviz.github.io/>)
        - Other examples: <https://github.com/collections/github-pages-examples>
- Think about files over github limit (100MB?).

# Workset file format
- Fields we may want to use:
    - `briefDescription`
    - `fullDescription`
    - `creator` // name, email, affiliation. How to model in JSON?
    - `created` 
    - `publisher`? HTRC?
    - `title`
    - `description` cf. `briefDescription`, `fullDescription`
    - `languages`
    - `contributer`? HTRC staff?
    - `subject`
    - `extent`
    - `visibility`

- What does this message mean when downloading a workset: “The downloaded workset will contain only 906 volumes out of the total(919 volumes).”? 
- Workset CSV includes titles. JSON does not. Titles would be useful for someone who wanted to browse the workset in the github repository. Could we include the titles in the JSON-LD? We could include both the JSON-LD and CSV, but that seems confusing to for users--two different data formats representing the workset, but each with different data. If we got titles into the JSON-LD it would be complete: metadata about the workset, and the list of IDs with titles.


# Derived datasets

**General idea:** Come up with two or three derived datasets that we can generate for _all_ SCWAReD projects. Then we know we will deliver that part of the deliverable, and there will be some consistency among the SCWAReD packages. If scholars generate additional datasets, of course, we will use those as well. Also, we can re-use READM.md files across all the packages.

Possibilities:

- names entity data
- geographic data w/ coordinates
- genre data
- sentiment data

Issues:

- get scholar approval to include these in packages.
