# datagen

<?xml version="1.0" ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="content-type" content="text/html; charset=utf-8" />
<link rev="made" href="mailto:" />
</head>

<body>



<ul id="index">
  <li><a href="#NAME">NAME</a></li>
  <li><a href="#SYNOPSIS">SYNOPSIS</a></li>
  <li><a href="#DESCRIPTION">DESCRIPTION</a></li>
  <li><a href="#OPTIONS">OPTIONS</a></li>
  <li><a href="#EXAMPLES">EXAMPLES</a></li>
  <li><a href="#REQUIREMENTS">REQUIREMENTS</a></li>
  <li><a href="#SEE-ALSO">SEE ALSO</a></li>
  <li><a href="#AUTHOR">AUTHOR</a></li>
  <li><a href="#COPYRIGHT">COPYRIGHT</a></li>
  <li><a href="#LICENSE">LICENSE</a></li>
</ul>

<h1 id="NAME">NAME</h1>

<p>datagen - Generate data in multiple formats</p>

<h1 id="SYNOPSIS">SYNOPSIS</h1>

<pre><code>    perl datagen.pl [-inp=perl_code_snippet] [-dat_path=path]
                    [-dat_bname=str] [-dat_fmts=ext ...]
                    [-nofm] [-nopause]</code></pre>

<h1 id="DESCRIPTION">DESCRIPTION</h1>

<pre><code>    Using a set of columnar data, datagen can generate the following data files:
        [1] .dat  - Plain text
                    (in an aesthetically pleasing way)
        [2] .tex  - A LaTeX tabular environment
                    (in an aesthetically pleasing way)
        [3] .csv  - Comma-separated values
                  - A Third-party Perl module Text::CSV required
        [4] .xlsx - Microsoft Excel 2007
                    (in an aesthetically pleasing way)
                  - A Third-party Perl module Excel::Writer::XLSX required
        [5] .json - JavaScript Object Notation
                    A Third-party Perl module JSON required
        [6] .yaml - YAML
                    A Third-party Perl module YAML required</code></pre>

<h1 id="OPTIONS">OPTIONS</h1>

<pre><code>    -inp=perl_code_snippet (short: -i)
        A Perl code snippet specifying the data to be generated.
        Refer to the sample .gen files.

    -dat_path=path (short: -path, default: current working directory)
        The path in which the generated data files will be stored.

    -dat_bname=str (short: -bname, default: basename of -inp)
        The basename (filename without an extension) of
        to-be-generated data files.

    -dat_fmts=ext ... (short: -fmts, default: dat, xlsx)
        Data formats. Multiple formats are separated by the comma (,).
        all
            All of the following ext&#39;s.
        dat
            Plain text
        tex
            LaTeX tabular environment
        csv
            comma-separated value
        xlsx
            Microsoft Excel 2007
        json
            JavaScript Object Notation
        yaml
            YAML

    -nofm
        Do not show the front matter at the beginning of the program.

    -nopause
        Do not pause the shell at the end of the program.</code></pre>

<h1 id="EXAMPLES">EXAMPLES</h1>

<pre><code>    perl datagen.pl -i=sample1.gen -path=./reactor1 -fmts=all
    perl datagen.pl -i=sample2.gen -path=./reactor2 -bname=genshiro
    perl datagen.pl -i=sample3.gen -path=./inus -bname=shiba -nopause</code></pre>

<h1 id="REQUIREMENTS">REQUIREMENTS</h1>

<pre><code>    Perl 5
        Text::CSV, Excel::Writer::XLSX, JSON, YAML</code></pre>

<h1 id="SEE-ALSO">SEE ALSO</h1>

<p><a href="https://github.com/jangcom/datagen">datagen on GitHub</a></p>

<h1 id="AUTHOR">AUTHOR</h1>

<p>Jaewoong Jang &lt;jangj@korea.ac.kr&gt;</p>

<h1 id="COPYRIGHT">COPYRIGHT</h1>

<p>Copyright (c) 2018-2019 Jaewoong Jang</p>

<h1 id="LICENSE">LICENSE</h1>

<p>This software is available under the MIT license; the license information is found in &#39;LICENSE&#39;.</p>


</body>

</html>
