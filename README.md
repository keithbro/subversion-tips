# Subversion Tips

## Applying a patch (or diff) to your local codebase

From the directory in which the diff was created...

    patch -p0 -i ~/someone_elses_change.diff
    
Full article: https://ariejan.net/2007/07/03/how-to-create-and-apply-a-patch-with-subversion

## Reverting your local codebase to a given revision number

    svn merge -c -12345 .

Full article: http://wildebeestplain.blogspot.co.uk/2012/02/reverting-or-rolling-back-accidental.html
