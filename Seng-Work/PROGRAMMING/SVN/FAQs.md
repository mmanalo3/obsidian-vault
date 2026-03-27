# How to apply SVN ignore file to all directories?
- [i] execute `svn propset svn:ignore -R -F .svnignore .`

# How to verify SVN ignore properties?
- [i] execute `svn propget svn:ignore -R .`

# How to SVN add all changes?
- [i] execute `svn add . --force`

# How to SVN delete multiple file?
- [i] execute `svn status | grep '.cache$' | awk '{print $2}' | xargs svn delete --keep-local`

