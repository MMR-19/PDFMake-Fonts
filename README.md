# PDFMake fonts
The purpose of the repository is to include different font base64 files, that can be included on a javascript project, that uses **PDF Make** to build .pdf files, in a super easy way
Check the [PDF Make project!!](https://pdfmake.github.io/docs/)

The usage is quite simple!
Just add the `font.js` file after you load the `pdfmake.js` needed. Then set your style or your font on your text blocks!

## Load
Example for Times New Roman:
`<script src="yourDirectory/vfs_fonts_times.js"></script>`

## Usage
### 1) Define the font on the document acording to the **font table** below
```
pdfMake.fonts = {
    // All 4 components must be defined
    TimesNewRoman: {
        normal: 'Times-New-Roman-Regular.ttf',
        bold: 'Times-New-Roman-Bold.ttf',
        italics: 'Times-New-Roman-Italic.ttf',
        bolditalics: 'Times-New-Roman-BoldItalic.ttf'
    }
};
```
#### Please note that any change to the reference on the table will cause a malfunction.

### 2) Set the font on your text block
```
content:[  
      {  
         text: 'your text with Times New Roman font'
         font: 'TimesNewRoman'
      }
   ]
```
#### Optional: You can also set a custom style and set the style on a text block
```
{  
   styles:{  
      style_Times:{  
         fontSize: 22,
         bold: true,
         font: 'TimesNewRoman'
      }
   }
   content:[  
      {  
         text: 'your text using style'
         style: 'style_Times'
      }      
   ]
}
```

## Font Table
Javascript file | `normal` | `bold` | `italics` | `bolditalics`
--------------- | ------- | ---- | ------ | ----------
`vfs_fonts_times.js` | Times-New-Roman-Regular.ttf | Times-New-Roman-Bold.ttf | Times-New-Roman-Italic.ttf | Times-New-Roman-BoldItalic.ttf
