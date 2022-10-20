# theater-sharers
Archival data on shareholders in the 18th-century London theaters

## Introduction
This repository contains transcriptions of legal documents pertaining to shareholders in 18th-century London theaters. Mattie Burkert and Michele Pflug viewed and photographed the documents at the UK National Archives and the London Metropolitan Archive in the summer of 2022 with support from the Office of the Provost and the Dean's Office of the College of Arts and Sciences at the University of Oregon. The researchers then transcribed and began encoding a selection of documents in the fall of 2022 in Eugene, Oregon. 

This repository hosts Microsoft Word and XML files representing the completed and in-progress transcriptions and encodings, as well as tabular data representing notes towards a network analysis of individuals who were financially and/or legally entangled with the theater business in the period. 

Reference images for the project are currently hosted on [Mattie Burkert's University of Oregon webspace](https://pages.uoregon.edu/mburkert/). These images are intended for research purposes only and should not be duplicated, reproduced, published, or otherwise reused. 

## Contact Information of Researchers
- Principal Researcher: Dr. Mattie Burkert, Assistant Professor, Department of English, University of Oregon, mburkert@uoregon.edu
- Research Assistant: Michele Pflug, PhD Candidate, Department of History, University of Oregon, mpflug@uoregon.edu

## File Naming Conventions
- XML file names encode the source archive, shelfmark, and identity of uploader, in that order. For example NA_C8-599-74_MB refers to the UK National Archives reference C 8/599/74, uploaded by Mattie Burkert. 
- MSWord file names follow the order of archive, reference code, and “transcription” to indicate that the file has not yet been encoded. 

### Abbreviations used in file names: 
- NA = National Archives
- LMA = London Metropolitan Archives
- MB = Mattie Burkert
- MP = Michele Pflug 


## Methodology

### Photograph and Transcription Conventions:
- Transcriptions of the photographs follow the editorial conventions laid out on page 4 of [Heather Wolfe’s Alphabet Book](https://folgerpedia.folger.edu/mediawiki/media/images_pedia_folgerpedia_mw/7/79/AlphabetBook2020.pdf). The only exception is that “ff” was transcribed as “F”. 
- Since a single line of the archival document often consisted of several lines in MS Word, two carriage returns are used to separate each manuscript line. 
- IMG numbers, folio numbers, and notes are recorded in brackets. 
- Uncertain transcriptions are highlighted; yellow indicates a high degree of uncertainty and blue indicates moderate uncertainty. The source of uncertainty is not recorded in the transcription; it could derive from ambiguous letterforms or any manuscript characteristic that obscures the text (i.e. gaps, holes, creases, smudges, effacement, etc). The highlighted letter “x” is used as a placeholder for the estimated number of ambiguous or missing letters. 
- Footnotes are used sparingly to provide additional notes.


### Encoding Conventions: 
In September and October 2022, Mattie and Michele began encoding the documents using [LEAF-Writer editor](https://leaf-writer.leaf-vre.org/). They followed TEI Guidelines for encoding manuscripts and relied on the following resources: 

- [MsDesc](https://msdesc.github.io/consolidated-tei-schema/msdesc.html)
- [Text Encoding Initiative](https://tei-c.org/release/doc/tei-p5-doc/en/html/MS.html)
- [Folgerpedia: Dromio](https://folgerpedia.folger.edu/Dromio:_Folger_Transcription_Platform)

All tags for the theater-sharers project derive from MsDesc and TEI. The Folgerpedia resource provides side-by-side examples of a manuscript, the diplomatic transcription, and the XML. Therefore, it is a useful resource for beginners learning how to recognize and identify manuscript features. Theater-sharers, however, does not rely on Folgerpedia for tagging conventions. 

In the first iteration of encoding, Mattie and Michele decided to focus on encoding the textual features recorded in the semi-diplomatic transcription of the MS Word document. These features would not have been preserved if simply copy and pasted into a text file or XML editor. Tags used in this first iteration include: 

- `<lb/>` = line break
- `<expan>` = expansion of abbreviations
- `<unclear>` = unclear or missing text
- `<add>` = inter linear insertions
- `<p>` = paragraph breaks
- `<note>` = notes recorded at the beginning of MS document and in brackets
- `<del>` = deletion (strikethrough or any erasure)
- `&amp;` = amp

In this iteration, we opted for tags that recorded a general, as opposed to a specific, type of feature. For example, we decided to use the <expan> tag to describe any expansion of an abbreviation. We plan to add more specific tags for different types of abbreviations (brevigraphs, contractions, suspensions) at a later date. Similarly, the <unclear> tag denotes questionable or partly legible letters and any gaps, holes, creases, smudges, or deliberate or accidental effacements made to the text. Again, such specifications will be encoded at a later stage. 

Michele opted to encode the documents directly in MS Word, since most of the features recorded there were not preserved in her text editors or Leaf-Writer. Michele encoded one tag at a time in MS Word. The <expan> tag often required multiple proofreadings to capture all the abbreviations. She also did a find and replace action of the “&” symbol to replace it with “&amp;”. Then the encoded document was copied and pasted into the open source text editor Visual Studio Code for verification. Edits were made in the text editor to validate the code. The validated code was then uploaded to Leaf-Writer via copy and paste. Once in Leaf-Writer, the document was spot checked for any errors in spacing and then uploaded to the Github repository theater-sharers via Leaf-Writer. 

## Recommended next steps
1. Bibliographic descriptions of manuscripts
2. TEI headers for XML files 
3. Convert image numbers and folio numbers recorded in <note> tags to the appropriate tags
4. Encode missing attributes for <unclear> and <expan> tags


