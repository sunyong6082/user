# Markdown
# On this page:
- [GitLab Flavored Markdown (GFM)](##gitLab_flavored_markdown (GFM))
## GitLab Flavored Markdown (GFM)
>**Note:** Not all of the GitLab-specific extensions to Markdown that are described in this document currently work on our documentation website.  
For the best result, we encourage you to check this document out as rendered by GitLab: [markdown.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md)

GitLab uses (as of 11.1) the [CommonMark Ruby Library](https://github.com/gjtorikian/commonmarker) for Markdown processing of all new issues, merge requests, comments, and other Markdown content in the GitLab system. Previous content, wiki pages and Markdown files (.md) in the repositories are still processed using the [Redcarpet Ruby library](https://github.com/vmg/redcarpet).

Where there are significant differences, we will try to call them out in this document.

GitLab uses "GitLab Flavored Markdown" (GFM). It extends the standard Markdown in a few significant ways to add some useful functionality. It was inspired by [GitHub Flavored Markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/).

You can use GFM in the following areas:
* comments
* issues
* merge requests
* milestones
* snippets (the snippet must be named with a .md extension)
* wiki pages (currently only rendered by Redcarpet)
* markdown documents inside the repository (currently only rendered by Redcarpet)
* epics

You can also use other rich text files in GitLab. You might have to install a dependency to do so. Please see the [github-markup gem readme](https://github.com/gitlabhq/markup#markups) for more information.

## Newlines
>If this is not rendered correctly, see [https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#newlines](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#newlines)

GFM honors the markdown specification in how [paragraphs and line breaks are handled](https://daringfireball.net/projects/markdown/syntax#p).
A paragraph is simply one or more consecutive lines of text, separated by one or more blank lines. Line-breaks, or soft returns, are rendered if you end a line with two or more spaces:
```
Roses are red [followed by two or more spaces]           
Violets are blue

Sugar is sweet
```
Roses are red    
Violets are blue

Sugar is sweet
## Multiple underscores in words 
>If this is not rendered correctly, see [https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#multiple-underscores-in-words](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#multiple-underscores-in-words)

It is not reasonable to italicize just part of a word, especially when you're dealing with code and names that often appear with multiple underscores. Therefore, GFM ignores multiple underscores in words:
```
perform_complicated_task

do_this_and_do_that_and_another_thing
```
perform_complicated_task   
do_this_and_do_that_and_another_thing
## URL auto-linking 
>If this is not rendered correctly, see https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#url-auto-linking

GFM will autolink almost any URL you copy and paste into your text:
```
* https://www.google.com
* https://google.com/
* ftp://ftp.us.debian.org/debian/
* smb://foo/bar/baz
* irc://irc.freenode.net/gitlab
* http://localhost:3000
```
* [https://www.google.com](https://www.google.com/)
* [https://google.com/](https://google.com/)
* [ftp://ftp.us.debian.org/debian/](ftp://ftp.us.debian.org/debian/)
* smb://foo/bar/baz
* irc://irc.freenode.net/gitlab
* [http://localhost:3000](http://localhost:3000/)

## Multiline Blockquote 
>If this is not rendered correctly, see [https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#multiline-blockquote](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md#multiline-blockquote)

On top of standard Markdown [blockquotes](https://docs.gitlab.com/ee/user/markdown.html#blockquotes), which require prepending > to quoted lines, GFM supports multiline blockquotes fenced by >>>:
```
>>>
If you paste a message from somewhere else

that

spans

multiple lines,

you can quote that without having to manually prepend `>` to every line!
>>>
```
>>>If you paste a message from somewhere else  

that  
spans  
multiple lines,  
you can quote that without having to manually prepend > to every line!
>>>    

