# Anne of Green Gables: formatted 

Formatted versions of my <a href='https://johanley.github.io/anne-of-green-gables/index.html'>transcription of _Anne of Green Gables_</a>.

This repo was created mainly for producing items for Project Gutenberg.

The PG (HTML) version of the transcription is <a href='https://johanley.github.io/anne-of-green-gables-fmt/index.html'>here</a>.

This repo has a Creative Commons Zero v1.0 Universal license.
That's <a href='https://creativecommons.org/share-your-work/public-domain/cc0'>roughly equivalent to public domain.</a>

## Inputs to Project Gutenberg

Project Gutenberg has two main formats:
<ul>
 <li>a single plain text file (UTF-8, .txt extension), with standards on formatting
 <li>an XHTML file (as .html), used in turn to generate .epub and .mobi formats. 
 There are some general standards, but they aren't numerous.
 They focus on identifying chapters and ensuring basic XHTML/CSS validity.
</ul>

<a href='https://www.gutenberg.org/'>Project Gutenberg</a> (PG) works pretty closely with <a href='https://www.pgdp.net/c/'>Distributed Proofreaders</a> (DP). 
DP has a lot of good documentation about the required formats and standards (links below).
The general idea is to follow their recommendations, and to use validators before submitting files to PG.

### Main links
<ul>
 <li><a href='https://www.pgdp.net/wiki/DP_Official_Documentation:PP_and_PPV/Post-Processing_FAQ'>DP's Post Processing FAQ</a> - they refer to standardized formatting as post-processing (as in post proof-reading and post formatting).
 <li><a href='http://www.gutenberg.org/help/volunteers_faq.html'>Short summary from PG</a> 
 <li><a href='https://copy.pglaf.org/index.php'>PG Copyright Clearance</a> - the start of their process. They will send you a 'clearance key' when approved; you need that to upload the book to PG.
 <li><a href='https://upload.pglaf.org/index.php'>PG upload for your .zip </a> 
 <li><a href='https://ebookmaker.pglaf.org/index.php'>PG Bookmaker tool</a> 
 <li><a href='https://validator.w3.org/'>W3C XHTML validator</a> 
 <li><a href='http://jigsaw.w3.org/css-validator/'>W3C CSS validator</a> 
 <li><a href='http://www.gutenberg.org/ebooks/61236'>Emily of New Moon</a> - an example to follow, for formatting. 
      It likely used <a href='https://archive.org/details/emilyofnewmoon00mont_1/page/n7/mode/2up'>this copy-text</a>.
</ul> 

After you submit files to PG, they will be examined closely by <b>PG whitewashers</b>, who prepare the text for final publication.
File names are formatted

<P><tt>like_this_or-that-01.txt</tt>

<P>all in lower case.

<P>When you upload, you zip together all of the formats you have into a single zip file.
There are validators that you can use to help you through the process.

<P>Distributed Proofreaders acts as the main input into Project Gutenberg. 
They have tons of information on what is required:
<ul>
 <li><a href='https://www.pgdp.net/wiki/DP_Official_Documentation:PP_and_PPV/Post-Processing_FAQ'>Post Processing FAQ</a> - they refer to standardized formatting as post-processing (as in post proof-reading and post formatting).
 <li><a href='https://www.pgdp.net/wiki/PPTools/Ppgen'>ppgen</a> - their tool that generates both the plain text and HTML versions from a common source
 <li>pptext - checks the output of ppgen
 <li><a href='https://www.pgdp.net/wiki/DP_Official_Documentation:Formatting/Formatting_Guidelines'>DP Formatting Guidelines</a>
 <li><a href='https://www.pgdp.net/wiki/DP_Official_Documentation:Formatting/Formatting_Guidelines#p_errors'>DP Errors and Misspellings</a>
</ul>

### Three main parts

There are 3 main parts (wrapped later by PG boilerplate):
<ul>
 <li>front matter
 <li>main body (38 chapters, in this case)
  <ul>
   <li>plain text
   <li>poetry
   <li>letters
   <li>illustrations
  </ul> 
 <li>transcriber's notes, at the end
</ul>

### Process

Make a branch called <a href='https://github.com/johanley/anne-of-green-gables-editions/tree/1908-LCP-4th-pg'><em>1908-LCP-4th-pg</em></a> off the uncorrected branch, to hold the desired text.
Apply a small number of corrections to that branch.

<P>After that, the text needs to be formatted for PG.
My formatting is only semi-automated:
<ul>
 <li>create a template file to hold the title page, transcriber notes and so on, entered manually
 <li>run a script (Java, in Eclipse, against the correct branch) to inject the bulk of the text into the template file (with line wrap at 72)
 <li>apply <em>manual formatting for poetry and correspondence</em>
 <li>run final sanity checks (scripts) to see if I've added unwanted characters in my manual edits (just to be sure)
 <li>zip the result and send it to PG
</ul>

### Poetry/Correspondence

These are special places where I need to format the text manually.

<P>P: poetry, L: correspondence (a letter).

<P>
<ul>
 <li>dedication: P
 <li>Ch 02: P little birds sang
 <li>Ch 07: L (odd, starts as normal text) Gracious Heavenly Father
 <li>Ch 11: P Midian
 <li>Ch 17: 2P, 2L; when twilight drops; shorn of Brutus
 <li>Ch 18: P nothing but death
 <li>Ch 19: P not a sister
 <li>Ch 24: P heart farewell (not special, inline!)
 <li>Ch 29: P stubborn spearsmen
 <li>Ch 31: P hills peeped
 <li>Ch 32: L (embedded in normal text, long)
 <li>Ch 33: P one moonbeam
</ul>


### Text requirements/recommendations

<ul>
 <li>UTF-8 encoding, .txt extension
 <li>end of line is CR-LF (Windows style)
 <li>byte-order mark (BOM) removed (they strip it out if present; don't worry about it)
 <li>line width 60-70, max 75 (recommend 72)
 <li>italic like _this_, bold like =this=
 <li>using em-dash is OK
 <li>using curly quotes is OK
 <li>no tab characters allowed
 <li>no spaces at end of lines
 <li>no extra spaces between words
 <li>use ligatures when the source copy-text does
 <li>match the copy-text closely, including errors; they can be noted in the transcriber's notes
 <li>it's ok to end a line in <em>Mr.</em> or <em>Mrs.</em>; no need for a non-breaking space - <a href='http://www.gutenberg.org/files/64216/64216-0.txt'>example</a>
 <li> 4 empty lines: at very top (gap after PG boilerplate)
 <li> 4 empty lines: at the top of a chapter
 <li> 4 empty lines: between frontispiece and title page
 <li> 2 empty lines between chapter headings and chapter body
 <li> hyphens at the end of the line: compare the spelling of the same word as found elsewhere in the text
 <li> transcriber's note at the end; this helps to flag items to PG whitewashers
 <li> poetry: indent by 1-4 spaces, so that line wrapping by tools is turned off
 <li> blockquotes: treat as poetry
 <li> letters/correspondence? those are trickiest items
 <li> front matter: seems to be some freedom there, as long as it's reasonable
</ul>

<P>Line-width/line-wrapping is a bit tricky. Be careful with that.
(Java has a BreakIterator class, but it's a bit quirky in its behaviour.)

<P>In my case, most items are auto-generated. Poetry and letters are two items 
that are handled manually, by editing the generated output. 

### HTML requirements/recommendations
<ul>
 <li>UTF-8 encoding
 <li>XHTML 1.0 Strict or 1.1 (epub uses XHTML)
 <li>modern <a href='https://www.gutenberg.org/files/2814/2814-h/2814-h.htm'>example</a>
 <li>CSS 2.1 or below; CSS 3 can also be used if needed; CSS appears to be embedded, not in a separate .css file
 <li>use W3C validators for markup and CSS; use HTML Tidy; remove unused styles
 <li>use PG's ebookmaker converter to convert your book and review the result carefully (checks epub/mobi formats)
 <li>image file formats: .jpg (.png for vector drawings)
 <li>font: not specific, font-family only
 <li>don't use: &lt;br&gt; (except in poems?), &amp;nbsp;, or empty tags to control spacing; use CSS margin, padding
 <li>title: H1
 <li>chapter: H2
 <li>images are placed in a conventional <em>images</em> directory beside the html
 <li>cover image: no larger than 256K, width-height from 650x1000 to 5000x5000. Name is cover.jpg.
 <li>inline image: no larger than 256K, up to 5000x5000
 <li>example of title-tag: <em>The Project Gutenberg eBook of Alice's Adventures in Wonderland, by Lewis Carroll</em>
 <li>metadata or comments about the text can be placed in the header, or in HTML comments
 <li>page numbers optional, not mandatory; some people put them in comments
 <li>no external links allowed
 <li>css: div.chapter, p.poem, p.letter
 <li>the text flow uses max width similar to plain text files
</ul>

The PG (HTML) version of the transcription is deployed <a href='https://johanley.github.io/anne-of-green-gables-fmt/index.html'>here</a>.
