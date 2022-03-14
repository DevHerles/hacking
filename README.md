# pdftk
## merge pdfs
```bash
pdftk file1.pdf file2.pdf cat output merged-files.pdf
```

## extract pages
Extract pages 12 to 15

```bash
pdftk full-pdf.pdf cat 12-15 output outfile_p12-15.pdf
```

### bonus
If I want to extract pages 1-10, 15, and 17?
```bash
pdftk A=full-pdf.pdf cat A1-10 A15 A17 output extracted-pages.pdf
```

## rotate pdfs
- Rotate page 1 by 90 degrees clockwise:

```bash
pdftk in.pdf cat 1east output out.pdf
```

- To rotate all pages clockwise:
```bash
pdftk in.pdf cat 1-endeast output out.pdf
```
### Note:
The `east` etc. is meaningful if you want other rotations. From the man page:

The page rotation setting can cause pdftk to rotate pages and documents. Each option sets the page rotation as follows (in degrees): north: 0, east: 90, south: 180, west: 270, left: -90, right: +90, down: +180. left, right, and down make relative adjustments to a page’s rotation.
