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
List of available name ids
```
    const NAME_COPYRIGHT          = 0;
    const NAME_NAME               = 1;
    const NAME_SUBFAMILY          = 2;
    const NAME_SUBFAMILY_ID       = 3;
    const NAME_FULL_NAME          = 4;
    const NAME_VERSION            = 5;
    const NAME_POSTSCRIPT_NAME    = 6;
    const NAME_TRADEMARK          = 7;
    const NAME_MANUFACTURER       = 8;
    const NAME_DESIGNER           = 9;
    const NAME_DESCRIPTION        = 10;
    const NAME_VENDOR_URL         = 11;
    const NAME_DESIGNER_URL       = 12;
    const NAME_LICENSE            = 13;
    const NAME_LICENSE_URL        = 14;
    const NAME_PREFERRE_FAMILY    = 16;
    const NAME_PREFERRE_SUBFAMILY = 17;
    const NAME_COMPAT_FULL_NAME   = 18;
    const NAME_SAMPLE_TEXT        = 19;
```

# Why this?
I found that `php-font-lib` has some strange issues with certain fonts, It retrieves strange chinese text instead of the real font name, postscript or family.

## Note
This is a fixed and slightly developed version of ttfinfo class, found here http://www.phpclasses.org/browse/package/2144.html
