# CAP Sample Volumes Arkansas
Two sample casebook volumes from Arkansas digitized in the Caselaw Access Project. 

## These are the two books included in this repository

### Volume 32044078573896
-  Ark. (Arkansas Reports) 
-  Volume 21
-  Published in 1860
-  Published By Johnson & Yerkes

### Volume 32044078577194
-  Ark. (Arkansas Reports) 
-  Volume 288
-  Published in 1986
-  Published By The State of Arkansas

## This is how each volume is structured
### Contents:
#### For each volume:
- One METS XML file with all volume-level metadata (~ 1 MB avg)
- One md5 file which contains an md5 checksum of the volume

#### For each page side:
- One 1-bit tiff (~60 KB avg)
- One ALTO v3 XML file (~75 KB avg)
    - Contains OCR with on-page word coordinates, separation into text blocks and text lines, and some content tagging
- One lossless jp2 (~2.5 MB avg)
  - Not available in this sample repository 

#### For each case:
- One METS XML file, which includes the text of each case body, and all case-level metadata 
     - These files contain a bunch of stuff, including:
       - Case text in a format simpler than the ALTO files
       - Descriptive metadata 
       - Processing and rights metadata
       - Structural data such as the images and alto files associated with the case.
    - (~75 KB avg)
### Naming Conventions:
- #### Volume-level files:
   - `(volume barcode)_redacted_METS.(xml/md5)`

-  #### Case-level files:
   - `(volume barcode)_redacted_CASEMETS_(case number).xml`
     - The case number is based on the order of the cases in the volume.
-  #### Page-level files:
   - Alto XML (v3): `(volume barcode)_redacted_ALTO_(leaf no)_(page side).xml`

   - Page Images: `(volume barcode)_(leaf number)_(page side).(tif/jp2)`
     - The leaf number is a count of each two-sided paper leaf.
     - The page-side specifies the front (0) or back (1) of the leaf.
     - A simple sequence number can be generated using `(leaf number) - 1 + (page_side)`. For example, 32044078577194_00005_0.tif is the 9th image in the volume, so 5 - 1 + 0 = 9.

Thoughts? Ideas? Hate mail? Tell us! Feel free to file an issue, or send us an email at lil@law.harvard.edu.