# ds-advances.github.io

The DALI current webpage.

This repository contains the current DALI conference page. Once the year has past it can be archived to dali20XX and modified to form the next year's page.


## Archiving Last Year's Page

Each year the main web page needs to be archived to store as a previous year's conference. To do this, the first thing you need to do is duplicate this repository. 

1. Create the new repo in github by going to <https://github.com/organizations/ds-advances/repositories/new>, use the name coding `ds-advancesXXXX` where `XXXX` is the year of the archived conference. 

2. Give the conference a description, "Web page for the XXXX Advances in Datascience Conference"

3. Do *not* create an initial README for the conference. 

4. Create the Repo.

5. Go to a suitable directory on your machine and type:

```
git clone --bare https://github.com/ds-advances/ds-advances.github.io.git
mv ds-advances.github.io.git ds-advancesXXXX
cd ds-advancesXXXX
git branch -m gh-pages
git push --mirror https://github.com/ds-advances/ds-advancesXXXX.git
```
6. Edit the `_config.yml` file in the new repo to set `baseurl` to `ds-advancesXXXX` and set `permalink` to  `"/:title.html"`.

7. Delete CNAME from the repo.

8. Commit the changes and push the repo.

9. Check that the archived page appears online at http://www.ds-advances.org/ds-advancesXXXX/

10. Update the original main repository at [https://github.com/ds-advances/ds-advances.github.io](https://github.com/ds-advances/ds-advances.github.io) for the current conference.
This will be used to host the current DALI.

11. Add the team `ds-advancesXXXX` to the admin rights for the repo `ds-advancesXXXX`

12. Create a new admin team for this year's page, `ds-advancesYYYY`, where `YYYY=XXXX+1` and assign it to admin `ds-advances.github.io` 

## More information

* See
  a list of repositories of past web sites [here](https://github.com/ds-advances/).

* This link gives [Github help about project
pages](https://help.github.com/articles/user-organization-and-project-pages/)
(at the bottom), if we put the Jekyll files in **gh-pages** branch, the repository
will be served under http://ds-advances.github.io/ds-advancesXXXX. Note that the main
repository uses master branch, not gh-pages.

* When archiving to ds-advancesXXXX, it is necessary to modify the ``baseurl``
  entry of ``_config.yml`` from ``baseurl: ""`` to ``baseurl: "/ds-advancesXXXX"``
so that internal links in the web site are generated correctly.  

* ``baseurl:
""`` is used only in the current site because its files are at the root
of ds-advances.github.io.
