
Note about building the PDF files:

1. Run   latex main6x9.tex   *twice*  to generate the correct table of contents.
2. Run   makeindex main6x9.idx   to generate the index.
3. Run   latex main6x9.tex   *again* to incorporate the index.
4. Run   dvipdf main6x9.dvi   to make the PDF.  The file will be named main6x9.pdf.
 

This builds a 6-by-9 inch PDF.   For the 8.5-by-11 inch PDF, repeat the above, 
replacing   "main6x9"   with  "main"

(Note that for me, latexpdf doesn't seem to handle the EPS graphics files 
that are used in the book.)

For the old lulu.com version, the following commands were used to convert the dvi file to
PDF, to properly embed all fonts (probably no longer needed):

    dvips -Ppdf -D 600 -G0 main6x9.dvi
    ./myps2pdf main6x9.ps
