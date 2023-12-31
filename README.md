# pdfsquash

Tool(s) to transform PDFs for printing multiple pages on a sheet.

## Usage
```bash
pdfsquash -o <output-pdf> <input-pdf-1> <input-pdf-2> ...
```

For more options, see
```bash
pdfsquash -h
```

## Examples
Following PDF files are used as sample inputs:
* [1.pdf](samples/1.pdf)
* [2.pdf](samples/2.pdf)
* [3.pdf](samples/2.pdf)
* [4.pdf](samples/2.pdf)

## Default options
```bash
pdfsquash -o samples/1-4-default.pdf \
    samples/1.pdf samples/2.pdf samples/3.pdf samples/4.pdf
```
Here is how result will look: [1-4-default.pdf](samples/1-4-default.pdf)

![image](https://github.com/pgmmpk/pdfsquash/assets/569458/28bb98eb-813d-48b8-ab1e-3c6c7c9a4358)

## Change spacing between minipages
Default spacing is 0. To chang it to 10pt use this command:
```bash
pdfsquash -o samples/1-4-spacing.pdf \
    -s 10 \
    samples/1.pdf samples/2.pdf samples/3.pdf samples/4.pdf
```
Here is how result will look: [1-4-default.pdf](samples/1-4-spacing.pdf)

![image](https://github.com/pgmmpk/pdfsquash/assets/569458/ca524df7-0dc2-4000-b123-6317e38d8437)

## Change page margin
Default page margin is 20pt. To change it to 0pt use this command:
```bash
pdfsquash -o samples/1-4-margin.pdf \
    -m 0 \
    samples/1.pdf samples/2.pdf samples/3.pdf samples/4.pdf
```
Here is how result will look: [1-4-default.pdf](samples/1-4-margin.pdf)

![image](https://github.com/pgmmpk/pdfsquash/assets/569458/e7a10859-c04d-43a0-9b7a-dba1d033507c)

## Keep aspect ratio of the original
By default, original mini-pages will be shrinked and stretched to fit the target sheet location,
**independently in X and Y direction***.
If you want to preserve original aspect, do this:
```bash
pdfsquash -o samples/1-4-keep-aspect.pdf \
    -m 0 \
    -k \
    samples/1.pdf samples/2.pdf samples/3.pdf samples/4.pdf
```
Here is how result will look: [1-4-keep-aspect.pdf](samples/1-4-keep-aspect.pdf)

![image](https://github.com/pgmmpk/pdfsquash/assets/569458/13d938db-420e-48ff-b2b5-048f7a05df5f)

## TODO
1. Support other paper sizes (currently hardcoded to US Letter)
2. Support other number of mini-pages per paper sheet (2, 6, 8). Currently do only 4 mini-pages per paper sheet.
3. Support page re-ordering. Currently mini-pages are placed in a fixed order (left-to-right, top-to-bottom).

## License
MIT
