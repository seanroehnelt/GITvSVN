Key workflow disconnects when moving from SVN to Git
-----------------------------------------------------

Using SVN, a common workflow I've used over the years, to track down when/where a bug was introduced, is to use Filemerge.app by comparing trunk and with a branch or tag that is knows to not contain the bug.

opendiff [SVN]/branches/known-branch-or-tag-without-bug/path/to/project/or/module_dir [SVN]/trunk/path/to/project/or/module_dir

In trunk I'll step backwards from the tip or head, or step forward from when the branch/tag was created and diff the directory trees. This might sound complex, but in many cases you can track down when something was introduced very quickly.

My new team on Git... 

In any case, I need to adapt my workflow, because with Git you only have one [and can only have one] single working copy at a time. I might be able to point to my .git repo from a peer directory and checkout a different branch but I'm not sure. In the meantime I'm going to just make a clone of the same repo ... or ... add a local filesystem remote and push my repo there maybe. Then I can have two working copies to compare with Filemerge.app.

What complicated this further is we don't have a single repo when we really should have all of our related projects code base in the same repo... that's a whole other story and train of thought. 

bah!


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

