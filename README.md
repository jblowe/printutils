STEDT printutils
================

```
This file contains notes on the tools used for generating the Dictionary & Thesaurus.

Requirements:
	Bash shell
	MySQL 5.1+
	Perl
	Python 2.7
	XeTeX (included in Tex Live 2013)
	The STEDT MySQL database (in a database called 'stedt')
	Some Perl modules

Perl modules required:
	Unicode::Normalize
	Template
	DBI::mysql

Update database credentials in:
	STEDTUtil.bk.pm (rename to STEDTUtil.pm)
	bib/db_creds.orig (rename to db_creds)

Primary tools:
	bib/makeRefs.sh: generates a TeX bibliography from the local STEDT database (srcbib table)
	frontmatter/makeFrontMatter.sh: takes '1col' or '2col' argument and generates draft frontmatter pdf in disExperiment1/tex/
	disExperiment1/makeFascOnly.sh: takes 'V F C' argument (V=volume, F=fascicle, C=chapter) and generates draft fascicle pdf in disExperiment1/tex/
	disExperiment1/shebang.sh: generates entire D-T in disExperiment1/tex/ (but doesn't run makeRefs.sh)
	nightlyShebang.sh: generates entire D-T (edit file to set location for pdf file)
```
