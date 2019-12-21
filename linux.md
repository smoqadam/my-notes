# Linux

#### Convert pdf to image:

```text
pdfimages -j input.pdf page
```

#### Compress PDF

```text
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
```

