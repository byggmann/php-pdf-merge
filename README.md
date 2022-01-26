# PDF Merge for PHP

PDF Merge library for PHP.

Install with composer:

`composer require byggmann/php-pdf-merge`


## Highlights

Pdf merging where orientation is set automatically.

Tested in Laravel4 & Laravel5 framework (but still can be used without any framework as standalone utility).

## Usage

```php
// Autoload composer classes...

// and now we can use library
$pdf = new \Jurosh\PDFMerge\PDFMerger;

// add as many pdfs as you want
$pdf->addPDF('path/to/source/file.pdf') // sets orientation automatically, "all" pages default 
  ->addPDF('path/to/source/file.pdf', 'all', 'vertical')
  ->addPDF('path/to/source/file1.pdf', 'all')
  ->addPDF('path/to/source/file2.pdf', 'all', 'horizontal');

// call merge, output format `file`
$pdf->merge('file', 'path/to/export/dir/file.pdf');
```

That's it!

Enjoy and leave star if you like it :)
