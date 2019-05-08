
# Kernel Linux

There are several guides for kernel developers and users. These guides can be rendered in a number of formats, like HTML and PDF. Please read Documentation/admin-guide/README.rst first.

In order to build the documentation, use `make htmldocs` or `make pdfdocs`.
The formatted documentation can also be read online at:

https://www.kernel.org/doc/html/latest/

There are various text files in the Documentation/ subdirectory, several of them using the Restructured Text markup notation.

Please read the Documentation/process/changes.rst file, as it contains the requirements for building and running the kernel, and information about the problems which may result by upgrading your kernel.

## Patch Submission Steps

### 1. Git Clone

`$ git clone git://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git`

### 2. Create a New Branch

`$ git checkout -b "new branch"`

### 3. Modify Your Files

You can also run this checkpatch script for check errors and warnings.  
`$ perl5.28.1 ./checkpatch.pl --no-tree -f ./module-internal.h`

### 4. Add Modificated Files

`$ git add <files>`

### 5. Commit and Deatil your Changes

`git commit -s -v`

### 6. Check your Commit

`$ git show HEAD`  
`$ git log`  
`$ git log --pretty=oneline --abbrev-commit`  
`$ git show --pretty=oneline --abbrev-commit HEAD`

### 7. Format your Patch

`$ git format-patch -o /tmp/ HEAD^`

### 8. Send patch over Email to your Mentor

`$ mutt -H /tmp/<patch file>`


