# Markdown
## GitLab Flavored Markdown (GFM)
>**Note:** Not all of the GitLab-specific extensions to Markdown that are described in this document currently work on our documentation website.
>For the best result, we encourage you to check this document out as rendered by GitLab: [markdown.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md)

GitLab uses (as of 11.1) the [CommonMark Ruby Library](https://github.com/gjtorikian/commonmarker) for Markdown processing of all new issues, merge requests, comments, and other Markdown content in the GitLab system. Previous content, wiki pages and Markdown files (.md) in the repositories are still processed using the [Redcarpet Ruby library](https://github.com/vmg/redcarpet).

Where there are significant differences, we will try to call them out in this document.

GitLab uses "GitLab Flavored Markdown" (GFM). It extends the standard Markdown in a few significant ways to add some useful functionality. It was inspired by [GitHub Flavored Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/).

You can use GFM in the following areas:

[*https://www.google.com](https://www.google.com/)

[*https://google.com/](https://google.com/)

[*ftp://ftp.us.debian.org/debian/](ftp://ftp.us.debian.org/debian/)

*smb://foo/bar/baz

*irc://irc.freenode.net/gitlab

*http://localhost:3000

*Multiline Blockquote 
