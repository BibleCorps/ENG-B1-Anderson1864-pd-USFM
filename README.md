# ENG-B1-Anderson1864-pd-USFM
Henry T. Anderson's 1864 "Civil War" New Testament

# Translator
The translator was **[Henry Tompkins Anderson](http://www.therestorationmovement.com/_states/dc/anderson.htm)** (1812-1872).
* Some attributions _mistakenly_ refer to the translator as **Harry Tompkins Anderson**.
* When the Greek text of **Codex Sinaiaticus** was first rendered into English, Anderson's NT was used for the wording.

# Source text
## The Internet Archive
* https://archive.org/details/thenewtestament00andeuoft

## Digital Christian Library
* A scanned facsimile of the 1866 edition was downloaded from DCL on 2009-10-21. 
* The DCL seems to no longer be online.
* The PDF file does not have a selectable text layer.
* Errors (now fixed) in the SFM files often coincided with the locations of word-wrap hyphens in the PDF.

## Modern reprints
### University of Michigan (Michigan Historical Reprint Series)
* A facsimile [reprint](https://www.amazon.co.uk/Testament-original-Greek-H-T-Anderson/dp/1418188247/) paper copy of Anderson's 1864 text "stereotyped and printed for the author" in 1866 by John P Morton & Co,, Louisville, KY.
* Though the reprint page size is 154mm x 234mm, the original was evidently a pocket edition with print area 67mm x 110mm, so there's a huge margin on every page.
* DavidHaslam purchased this item on 15 Aug 2009.

### Kindle edition
* See [THE NEW TESTAMENT](https://www.amazon.co.uk/NEW-TESTAMENT-T-ANDERSON-H-ebook/dp/B07CLJS8JQ/).

### SWORD module
* [CrossWire Bible Society](http://crosswire.org/) distributes a SWORD module for the Anderson NT.
* This needs to be replaced by one made from this more accurate digital text.
* An updated conf file has been provided as well as a freshly derived OSIS file.
* The glossary words have not been marked where they occur in the SFM text.

#### OSIS
The OSIS XML file was made by the following steps.
* Convert the SFM files to OSIS using [adyeths/u2o](https://github.com/adyeths/u2o) Python script.
* Open the OSIS file in **Notepad++**.
* Use the **XMLTools** plugin to _linearize_ and then _pretty print_ the XML.
* _Save the OSIS file_.
* Rearrange the OSIS file such that all the verse **sID** & **eID** milestones are _tidily_ aligned.
* Systematically move verse **eID** milestones to after the start of the next paragraph.
* Move 3 more verse **eID** milestones in **Romans** to after the respective titles in chapter 1.
* _Save the OSIS file again_.

The post-processing steps are required to prevent _orphaned_ verse tags when the SWORD module is displayed in **Xiphos** (e.g.). Though two of the steps were implemented by means of bespoke **TextPipe** filters, they are simple enough to be done by other means. They are not yet incorporated into CrossWire module tools.

# Status
* Corrections were made by detailed comparison with the PDF file from the DCL.
* Corrections are now substantially completed, though the complete absence of errors is not guaranteed. 

## Dedication and Preface
* The printed work included a **Dedication and Preface** after the original copyright page.

## Glossary
* There is a very short **word glossary** after the end of Revelation.

## Book titles
* The book titles in the printed work were in upper case.
* The SFM files have these in lower case.

### Other titles
* The letter to the **Romans** is structured in major sections and sections with titles.

### Paragraphs
* The **Anderson NT** is a paragraphed work.

### Italics
* Some words in the printed edition were styled in italics. These are now marked using `\add ...\add*`.

### Remarks
* Some missing verses have been noted by a remark line at that point in the SFM file.
* In all but one case, the text is simply in the previous verse.
* **Acts 8:37** was missing from the 1866 printing, without any explanatory footnote.

#### Emptyvss
Ignoring the complete OT, the output of SWORD utility **emptyvss** lists these verses:
```
Matthew 19:30
Acts 8:37
Acts 23:35
II Corinthians 4:18
II Corinthians 13:14
I Thessalonians 2:20
II Timothy 3:17
Hebrews 13:25
I Peter 1:25
I John 5:21
Jude 1:25
Revelation of John 4:11
```
