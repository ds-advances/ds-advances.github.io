# ds-advances.github.io

The Advances in Data Science current webpage.

Derived from https://github.com/sods/_confweb

This repository contains the current ADS conference page. Once the year has past it can be archived to ds-advancesXXXX and modified to form the next year's page.


## Archiving Last Year's Page

Each year the main web page needs to be archived to store as a previous year's conference. To do this, the first thing you need to do is duplicate this repository. 

1. Create the new repo in github by going to <https://github.com/organizations/ds-advances/repositories/new>, use the name coding `adsXXXX` where `XXXX` is the year of the archived conference. 

2. Give the conference a description, "Advances in Datascience XXXX"

3. Do *not* create an initial README for the conference. 

4. Make sure the repo is public.

5. Create the Repo.

6. Go to a suitable directory on your machine and type:

```
git clone --bare https://github.com/ds-advances/adsYYYY.git
mv ds-advances.github.io.git ds-advancesXXXX
cd ds-advancesXXXX
git branch -d gh-pages
git branch -m gh-pages
git push --mirror https://github.com/ds-advances/adsXXXX.git
```

Where YYYY is XXXX-1 (i.e. last year's conference)

6. Edit the `_config.yml` file in the new repo to set `baseurl` to `adsXXXX` and set `permalink` to  `"/:title.html"`.


8. Commit the changes and push the repo.

9. Check that the archived page appears online at http://www.ds-advances.org/adsXXXX/


11. Add the team `adsXXXX` to the admin rights for the repo `adsXXXX`

## More information

* See
  a list of repositories of past web sites [here](https://github.com/ds-advances/).

* This link gives [Github help about project
pages](https://help.github.com/articles/user-organization-and-project-pages/)
(at the bottom), if we put the Jekyll files in **gh-pages** branch, the repository
will be served under http://ds-advances.github.io/ds-advancesXXXX. Note that the main
repository uses master branch, not gh-pages.


