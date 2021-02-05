# TTFInfo
Retrieve data stored in a TTF files 'name' table in PHP

# How to use

```
$ttfInfo    = (new TTFInfo())->setFontFile('path/to/ttf/file');
$fontInfo   = $ttfInfo->getFontInfo();

$postscript = $fontInfo[TTFInfo::NAME_POSTSCRIPT_NAME];
$full_name  = $fontInfo[TTFInfo::NAME_FULL_NAME];
$family     = $fontInfo[TTFInfo::NAME_NAME];
$sub_family = $fontInfo[TTFInfo::NAME_SUBFAMILY];
```
# Why this?
I found that `php-font-lib` has some strange issues with certain fonts, It retrieves strange chinese text instead of the real font name, postscript or family.

## Note
This is a fixed and slightly developed version of ttfinfo class, found here http://www.phpclasses.org/browse/package/2144.html
