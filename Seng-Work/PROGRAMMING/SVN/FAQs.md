# How to apply SVN ignore file to all directories?
> execute `svn propset svn:ignore -R -F .svnignore .`

# How to verify SVN ignore properties?
> execute `svn propget svn:ignore -R .`

# How to SVN add all changes?
> execute `svn add . --force`

# How to SVN delete multiple file?
> execute `svn status | grep '.cache$' | awk '{print $2}' | xargs svn delete --keep-local`

/git: