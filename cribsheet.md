Version ;

LaTeX  and Tips 
================

``

l\>p4in

`texhash` & update LaTeX database& `[alt-C][space] ` & default character
`[alt-P]*2` & unnumbered section `[alt-P]2` & numbered
section`[alt-P]i ` & item`[alt-P]l` & list`[alt-P]e` &
enumerate`[alt-C][right]` & Capitalize`[alt-C][down]` &
capitalize`[alt-C][up]` & CAPITALIZE`[alt-C]p` & typewriter
font`[alt-S]5` & font-size normal, increase numbers for larger
font`[alt-S]n` & font-size normal`[F7]` & spellchecker&
`\discretionary{%1}{%2}{%3}` & `\slash{}` & Breakable slash, short cut
for `\discretionary{/}{}{/}``\filbreak` & prevent an item in a (for eg.)
bibliography list breaking across page breaks`\jobname` & the current
filename `\filename@ext` & the current filename & `\ldots ` & ellipsis
…` -- ` & en-dash – ` --- ` & em-dash — & `\; ` & a thick space`\: ` & a
medium space`\, ` & a thin space`\! ` & a negative thin space`\times` &
$\times$&

ll

**BibTeX** & `\usepackage[square,sort]{natbib} ` & in
preamble`\renewcommand\refname{References}` & in preamble to change
heading`\bibliographystyle{ametsoc.bst}` & declare the BibTeX style file
to use`\bibliography{abs,references}{} ` & in document where the
bibliography is to appear

`xdvi` Commands
===============

ll

`R` & refresh**n**`s` & scale`g`, **n**`g` & end, move to page **n**`n`,
**n**`n` & next page, **n**th next page`p`, **n**`p` & previous page,
**n**th prev. page`k` & toggle keep position`D` & toggle grid

`ssh` Commands
==============

ll

`?` & help`#` & display

  ---------- --------------------
   `ssh -X`   force X connection
  ---------- --------------------

`vi` Commands
=============

ll

`:com <name> [-range] [-nargs]` & create macro command`|` & separates
vim commands on same line`:sp` & split window`[w][down]`, `[w][up]`,
`[w]w` & move around windows`` :`" `` & comment`[f`], `[b]` & forward,
back screen`:g//norm J` & join every second line &

### vim split windows commands

``

|l|l|

`ww ` &

change to next

`wn ` &

new empty window

`wq ` &

quit window

`wc ` &

close window

`wx ` &

exchange windows

`w= ` &

equalize

`w+ ` &

increase

`w- ` &

decrease

`w_ ` &

maximise

`wo` &

make only window

`bash` Scripting and Commands
=============================

\>p2inp4in

`man` command `| col -b ` & Print plain `man` page (`col` filters `ANSI`
escapes)`grep -B3 -C3 ` & Find with context before and after`mktemp` &
Create unique temporary file& `dumpkeys > newkeyfile` & Dump current
keymap to a file `loadkeys newkeyfile` & Load new keymap from a file
`keycode 29 = Caps_Lock`\
`keycode 58 = Control` & Swap capslock and control &\
\
 & `showkey` & to display the codes of the key pressed `xkeycap` & to
set up modmap graphically

NB Read the keyboard and console howto! & & `u` & delete line`c` &
cancel command`d`, `<esc>-d` & delete character, word`w` & delete word
backwards`v` & quote character`t`, `alt-t` & transpose chars, words`f`,
`alt-f` & forward`a` & start of line`e` & end of line& `!!` & repeat
previous command `!n:k` & insert the `k`-th word of command `n` `!-n:k`
& insert the `k`-th word of `n`-th previous command `!-n:*` & insert all
the words but the `0`-th of `n`-th previous command & **System
Administration** & `service`, `/etc/init.d/*d` & start, stop and status
of daemons`chkconfig` & manipulate run levels`hwclock -r`, `-a`, `-w`,
`-s` & read, adjust, write to, set from the hardware clock`procmail`,
`fetchmail`, `sendmail` & mail processing`procinfo`, `top`, `uptime`,
`w`, `who`, `whoami` & information about the system`lsof`, `fuser` &
information about open processes`dmidecode` & hardware information
`siga` & System Information GAtherer — SuSE system info tool

& **Monitoring** & `netwatch`, `iptraf`, `iftop` & `mii-tool` &
interface information`ntop:3000` & &

`set bell-style none` & `set nobeep=1` & in `csh``xset b off` & in
X-window`Settings\rightarrowBell\rightarrowNone` & in `konsole` &
**Other useful stuff** & `x-friend`, `google-desktop` & desktop search&
&

Some thoughts to add: to render a man page to plain ascii use
`man man | col -b`

GMT Hints
=========

`pstext` input: (*x*, *y*, *size*, *angle*, *fontno*, *justify*, *text*)

`convert -density 150 -page A4 filename.ps filename.png`

`gmtset WANT_EURO_FONT true` to get europeaen character sets

cc

& \\217$\sigma$ & \\163$\Theta$ & \\161ü & \\370$\Delta$ & \\104&

cc

`@` & to toggle symbol font&

`wget` Options
==============

ll

`-p` & everything needed`-nH` & not under host directory`--cut-dirs=n` &
ignore leading directory tree`-r ` & recursive`-N` & timestamping`-np` &
no parent`-nv` & nonverbose`-Q` & quota& &

`rsync` Options
===============

`rsync [options] fromdir host:destdir`

ll

& `-r` & recursive`-t` & copy timestamps too`-u ` & update newer
only`-n` & test, don’t do it`-v` & verbose

Manipulating `PostScript` Documents
===================================

1.  StarOffice and OpenOffice

    1.  Creating a presentation from StarOffice

        1.  print as a .ps, using the trim option

        2.  Rotate using `` \
            `pstops -w0 -h0 1:0R\(0in,8.27in\) psfile > rotfile`

        3.  `pstopdf -g7930x5950 rotfile pdffile`

        Now it’s in a script `rotate.zsh`

    2.  Preparing figures for OpenOffice

        OpenOffice is very bad at eps figures. Turn them into JPEGs.
        Matlab JPEGs are very bad, print them as EPS and turn them into
        JPEGs with `gimp`. `gmt` does not make JPEGs, make eps figures
        and use `gimp`.

2.  Changing from EPS to PS

    Use epsffit\
    A4 595x842

    A5 421x595

    A6 297x421

    A7 210x297

    Using pstops

    `pstops ’2:0L@.65(21cm,0)+1L@.65(21cm,14.85)’ filename`

3.  Converting to Postscript

    `convert -density [density] fromfile.jpg tofile.ps `

    `density` here refers to number of pixels across? (see ImageMagick
    help pages)

    `convert -density 150 -units pixelsperinch` seems to work.

4.  Concatenating Postscript documents and creating a pdf

    `gs -q -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sOutputFile=``output-file-name input-file1 ``[ ``input-file2 ...`` ]` \
    Note that the `input-file*` can also be pdf files, and ps and pdf
    documents can be mixed in the arguments`.`

5.  Converting pdf documents to postscript: try using gs with
    -sDEVICE=pswrite.

6.  Reluctant documents

    1.  You might be able to print reluctant postscript files by
        converting them using `` \
        `ps2ps [-dLanguageLevel=1] ``fromfile tofile`

    2.  Postscript files that are very large can turn into fairly small
        pdfs if you use `ps2pdf`.

    3.  Huge files that are slow to display (render) might be able to be
        flattened with `gimp`. For existing PDF documents that might be
        very slow to render some pages (possibly with a huge unflattened
        figure on them):

        split up the document with `gs -dFirstPage=n -dLastPage=m`\
        `gimp` the offending pages, saving as postscript\
        join the document back together with `gs` (see concatenating
        above)

7.  Badly adjusted page offsets

    1.  For source from a LaTeX document: try
        `dvips -t letter -f <dvifile>`

    2.  Look for the `align.ps` file in the ghostscript package; there
        are instructions in there for adjusting the margins using `gs`.
        Create a `margin.ps` file containing

        %% $<<$ /.HWMargins [ml mb mr mt] /Margins [x y] $>>$
        setpagedevice\
        %% ml = L \* 72, mb = B \* 72, mr = R \* 72, mt = T \* 72,\
        %% x = (1 - H) \* 720.0, y = (V - 1) \* 720.0\
        $<<$ /.HWMargins [0 0 0 0] /Margins [-180 -360] $>>$
        setpagedevice

        with the appropriate margins then add the `margin.ps` file to
        the list of input files.

    3.  Consult some of these for the problems of A4 versus Letter size:

        -   <http://amath.colorado.edu/documentation/LaTeX/reference/faq/a4.html>

        -   <http://dam.mellis.org/2003/12/a4_vs_letter/>

        -   <http://mintaka.sdsu.edu/GF/bibliog/latex/LaTeXtoPDF.html>

StarOffice Options
==================

ll

`-minimized` & keep startup bitmap minimized`-help/-h/-?` & show the
help message and exit`-writer` & create new text document`-calc ` &
create new spreadsheet document`-draw ` & create new drawing`-impress `
& create new presentation`-math` & create new formula`-global ` & create
new global document`-web` & create new HTML document&

X-server Workarounds\
=====================

ll

`ssh -X` & `konsolekalendar --help` & `soffice -help/-h/-?` & don’t try
`--[option]` !`soffice -minimized ` & no splash screen&

Recording a CD
==============

[

Obsolete Comment: Star has a Creative CDRW. Speeds are 4,2,24 (writable,
rewritable, read). NOTE: Drive does not like fixating in dummy mode. The
SCSI emulator driver is susceptible to locking up the CD on this
configuration, requiring a power cycle reboot from time to time. ]

### Modules required

sg, sr\_mod, loop

### Blank a rewritable cd 

-   `cdrecord -v blank=fast dev=0,0`

Can blank and burn in the same command.

### Make a filesystem

-   `# For an ext2 filesystem`

-   `dd if=/dev/zero of=cdimage; mke2fs cdimage; mount -o loop cdimage /mnt; \` \
    `cp -a dir /mnt`

-   `# For an iso9660 filesystem`

-   `mkisofs -v -R -o cdimage dir`

-   `# Burn it`

-   `cdrecord -v speed=2 dev=0,0 cdimage`

Use `mkhybrid` for a filesystem which can be read by a Mac.

### In one go

To burn the contents of the directory `dir.` Note the double $-$ for the
`nice` and the final $-$ for the `cdrecord. `

`nice --18 mkisofs -J -R -r dir | cdrecord -v speed=2 dev=0,0 -`

00.00.0000

Rock Ridge extensions

global read permissions and root ownership

Joliet extensions

### Setting defaults

The default device and speed can be specified in the file
`/etc/default/cdrecord`, to shorten the above commands, e.g.

-   `nice --18 mkisofs -J -R -r dir | cdrecord -v -`

-   `cat /etc/default/cdrecord`\
    `CDR_DEVICE=0,0,0 ` \
    `CDR_SPEED=2`


