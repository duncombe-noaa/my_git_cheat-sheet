# My GIT Cheat Sheet

##<a name="git"></a> Git commands

`git log --pretty=oneline --abbrev-commit <path>` 

short hand: `git log --oneline <path>`

`git log  --graph <path>`

Fix ANSI escape codes in `git log`: `git config --global core.pager "less -R"`

### Git Cheatsheets and Tutorials

- [Atlassian tutorials](https://www.atlassian.com/git/tutorials/)
- [NDP Interactive Cheat Sheet](http://ndpsoftware.com/git-cheatsheet.html)
- [Git Fix Um](http://sethrobertson.github.io/GitFixUm/fixup.html)
- [How to escape a git mess](http://justinhileman.info/article/git-pretty/git-pretty.png)
- [Think like a git](http://think-like-a-git.net/)
- [git ready](http://gitready.com/)
- [A github workflow to consider](http://blog.spreedly.com/2014/06/24/merge-pull-request-considered-harmful/#.VGerbPnF98E)
- [Git Best Practices](http://sethrobertson.github.io/GitBestPractices/)

##<a name="markdown"></a> Markdown

Closely associated with github is [Markdown](http://daringfireball.net/projects/markdown/syntax). Here are some cheatsheets and helps:

- [Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Markdown-Here-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet)
- [github-flavored-markdown](https://help.github.com/articles/github-flavored-markdown/)   

##<a name="powershell"></a> Powershell Commands

|Powershell command| Unix equivalent|
|---|---|
| `get-help` | `man` |
| `remove-Item` | `rm` |
| `remove-Item -recurse -force ` | ` rm -rf ` |


##<a name="python"></a>Python Wisdom

[Do not use --pylab flag for IPython](http://nbviewer.ipython.org/github/Carreau/posts/blob/master/10-No-PyLab-Thanks.ipynb)   
When you need to see a notebook without re-executing, trust notebooks with     
``` ipython trust mynotebook.ipynb [other notebooks.ipynb]```   
to generate a new signature (git repositories?). [Explanation here](http://ipython.org/ipython-doc/dev/notebook/notebook.html).  

``` conda list --revisions ```

Working with Wakari: be careful that your packages do not update `ipython` or `ipython-notebook`. This may break the Wakari installation.


###Python Resources<a name="python_resources"></a>

- [Think Python](http://www.greenteapress.com/thinkpython/html/index.html)
- [Dive into Python](http://www.diveintopython.net/index.html)
- [Learn Python the Hard Way](http://learnpythonthehardway.org/book/index.html) 

Python for Matlab Users (tutorials and advocacy):

- [Numpy for matlab users](http://wiki.scipy.org/NumPy_for_Matlab_Users)
- [A python primer for matlab users](http://bastibe.de/2013-01-20-a-python-primer-for-matlab-users.html)
- [Advantages of python over matlab](http://phillipmfeldman.org/Python/Advantages_of_Python_Over_Matlab.html) (Some of this the author is reaching!)    
- [10 Reasons](http://www.stat.washington.edu/~hoytak/blog/whypython.html)    

Possibilities:
- [Pyzo](http://www.pyzo.org/index.html)


## SSH problems?

This list from [stackexchange](http://stackexchange.com/) solved a login problem on CentOS :
- Your home directory `~`, your `~/.ssh` directory and the `~/.ssh/authorized_keys` file on the remote machine must be writable only by you: `rwx------` and `rwxr-xr-x` are fine, but `rwxrwx---` is no good,  even if you are the only user in your group (if you prefer numeric modes: 700 or 755, not 775).
If `~/.ssh` or `authorized_keys` is a symbolic link, the canonical path (with symbolic links expanded) is checked.
Your `~/.ssh/authorized_keys` file (on the remote machine) must be readable (at least 400), but you'll need it to be also writable (600) if you will add any more keys to it.
- Your private key file (on the local machine) must be readable and writable only by you: `rw-------`,`i.e. 600.
- Also, if SELinux is set to enforcing, you may need to run `restorecon -R -v ~/.ssh` (see e.g. Ubuntu bug 965663 and Debian bug report #658675; this is patched in CentOS 6 [*actually, no, it's not*]).

##<a name="vms"></a> Virtual Machines

[http://superuser.com/questions/73488/run-a-virtual-machine-from-virtualbox-without-launching-virtualbox?rq=1]

[http://superuser.com/questions/539880/using-virtual-box-is-it-possible-to-set-your-virtual-machine-time-to-be-differen]

## Miscellaneous Stuff

- Kill a tree and print from Github? [Read this](https://gitprint.com/).  
- Install and use git as a non-root user? [Read this](http://joemaller.com/908/how-to-install-git-on-a-shared-host/).   
- Want a private or company Github-like server? [Read this about gitlab](https://about.gitlab.com/gitlab-ce/) or [this about gitorious](http://getgitorious.com/). 
- Back up gmail, possibly fetch mail off gyre?  [Investigate](http://gmvault.org/download.html)


![Tree killer](images/04142010inset2.jpg) 



