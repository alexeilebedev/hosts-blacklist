Update /etc/hosts blacklist from the following URL

https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts

Features:
1. Accepts only blacklist entries (0.0.0.0)
2. Updates /etc/hosts in-place, using a marker to separate local
  content from downloaded content.
3. Some sanity checks on the size of downloaded data

I use a git repo under /, with "*" for .gitignore.
Then I manually add important system files, such as everything under /etc,
to the repo. Because of this design, the it's always possible to go back
with 'git checkout'. That's why no backup file is created on update.
