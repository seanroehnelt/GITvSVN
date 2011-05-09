Subversion (SVN)          Git 
========================  ===========================================================================
svn status                git fetch (pull commit info from remote repo but don't update working copy)
                          git status (local repo status only if not preceeded by 'git fetch')
________________________  ___________________________________________________________________________
svn update                git pull
________________________  ___________________________________________________________________________
svn commit                git commit 
                          git push 
________________________  ___________________________________________________________________________
svn revert file-name      git checkout file-name
________________________  ___________________________________________________________________________
<move local changes       git rebase master
aside; 'svn update' to 
tip of trunk then merge 
local changes back onto
working copy after
merge operation>
________________________  ___________________________________________________________________________

