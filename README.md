# awesome-git
## To create a new empty master branch
```bash
$> git checkout --orphan master
$> git rm -rf *
```
## Change commit date of a specific commit
```bash
$> git filter-branch --env-filter \
   "if test \$GIT_COMMIT = 'e6dbcffca68e4b51887ef660e2389052193ba4f4'
   then
      export GIT_AUTHOR_DATE='Sat, 14 Dec 2013 12:40:00 +0000'
      export GIT_COMMITTER_DATE='Sat, 14 Dec 2013 12:40:00 +0000'
   fi"
```
