# Subversion Tips

## Creating a diff

What? Creates a text file contains the changes made in your local codebase.

Why? This can be useful when you want to share your changes with someone else.

    svn diff > my_changes.diff

## Applying a diff

What? Applies changes recorded in the diff your local codebase.

Why? Sometimes it's easier to review someone else's changes on your own development machine than it is to read the changes in code review applications.

From the directory in which the diff was created...

    patch -p0 -i ~/someone_elses_change.diff
    
Full article: https://ariejan.net/2007/07/03/how-to-create-and-apply-a-patch-with-subversion

## Reverting a specific commit

What? This will revert the changes made in a single revision.

Why? A change is causing problems and should be undone.

Note, it does not reverts the revision, it doesn't revert TO the revision. After this is done, you will still need to commit the changes.

    svn merge -c -12345 .

Full article: http://wildebeestplain.blogspot.co.uk/2012/02/reverting-or-rolling-back-accidental.html
