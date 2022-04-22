# Challenge to decipher this file
This is a challenge to decipher a proprietary binary file "FS1.mss". The file was created by me using an instrument of a commercial vendor. For interoperability, I want to read all the content of the measurement.

## Goal
Create an x-y plot of 'Specimen/cukxxwvnejp/RawData/DisplacementIntoSurface' vs. 'Specimen/cukxxwvnejp/RawData/LoadOnSample' favorably by python.

## How to claim eternal glory?
Post the solution as issue. The first complete solution wins.

## What I gathered?
- The file is an OLE2 compound document storage and there are multiple separately compressed streams inside. The streams start with either of two byte-sequences. 
- The streams that start with BE D0 BE D0 contain numbers (doubles or ints) while the other streams contain likely XML-strings. The very short BED0BED0 streams contain short-ints possibly. All uncompressed BE D0 BE DO streams should have the same length.
- The vendor executable that writes the files references the PK trademark and some function calls contain the word 'implode' (via Ghidra string scan). This also might be a red herring.

May the best person win.


