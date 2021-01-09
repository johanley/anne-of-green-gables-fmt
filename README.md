# Anne of Green Gables: formatted 

Formatted versions of my <a href='https://johanley.github.io/anne-of-green-gables/index.html'>transcription of _Anne of Green Gables_</a>.

This repo was created mainly for producing items for Project Gutenberg.


## Inputs to Project Gutenberg

Project Gutenberg has two main formats:
<ul>
 <li>a single plain text file (UTF-8, .txt extension), with standards on formatting
 <li>an XHTML file (as .html), used in turn to generate .epub and .mobi formats. 
 There are some general standards, but they aren't numerous.
 They focus on identifying chapters and ensuring basic XHTML/CSS validity.
</ul>

Main links needed:
<ul>
 <li><a href='https://www.pgdp.net/wiki/DP_Official_Documentation:PP_and_PPV/Post-Processing_FAQ'>DP's Post Processing FAQ</a> - they refer to standardized formatting as post-processing (as in post proof-reading and post formatting).
 <li><a href='http://www.gutenberg.org/help/volunteers_faq.html'>Short summary from PG</a> 
 <li><a href='https://copy.pglaf.org/index.php'>PG Copyright Clearance</a> - the start of their process
 <li><a href='https://upload.pglaf.org/index.php'>PG upload for your .zip </a> 
 <li><a href='https://ebookmaker.pglaf.org/index.php'>PG Bookmaker tool</a> 
 <li><a href='https://validator.w3.org/'>W3C XHTML validator</a> 
 <li><a href='http://jigsaw.w3.org/css-validator/'>W3C CSS validator</a> 
 <li><a href=''> </a> 
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
</ul>

Text requirements/recommendations:
<ul>
 <li>UTF-8 encoding, .txt extension
 <li>end of line is CR-LF (Windows style)
 <li>byte-order mark (BOM) removed (they strip it out if present; don't worry about it)
 <li>line width 60-70, max 75 (recommend 72)
 <li>italic like _this_, bold like =this=
 <li>using em-dash is OK
 <li>using curly quotes is OK
 <li>no tab characters allowed
 <li>use ligatures when the source copy-text does
 <li>no spaces at end of lines
 <li>no extra spaces between words
 <li> 4 empty lines: at very top (gap after PG boilerplate)
 <li> 4 empty lines: at the top of a chapter
 <li> 4 empty lines: between frontispiece and title page
 <li> 2 empty lines between chapter headings and chapter body
 <li> hyphens at the end of the line: compare the spelling of the same word as found elsewhere in the text
 <li> transcriber's note at the end; this helps to flag items to PG whitewashers
 <li> poetry: indent by 1-4 spaces, so that line wrapping by tools is turned off
 <li> blockquotes: treat as poetry
 <li> letters/correspondence?
</ul>

HTML requirements/recommendations:
<ul>
 <li>UTF-8 encoding
 <li>XHTML 1.0 Strict or 1.1 (epub uses XHTML)
 <li>modern <a href='https://www.gutenberg.org/files/2814/2814-h/2814-h.htm'>example</a>
 <li>CSS 2.1 or below; CSS 3 can also be used if needed; CSS appears to be embedded, not in a separate .css file
 <li>use W3C validators for markup and CSS; use HTML Tidy; remove unused styles
 <li>use PG's ebookmaker converter to convert your book and review the result carefully (checks epub/mobi formats)
 <li>image file formats: .png and .jpg
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

