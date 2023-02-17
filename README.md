# PDF_examples
This project should collect various PDF examples files with various defects for
testing purposes.

## Stream_Length
This folder contains all PDF files where **/Length** key is broken (for example
missing, incorrect length, etc.)

**[correct_length.pdf](Stream_Length/Non-compressed/correct_length.pdf)** - This
is just reference file with correct **/Length** and uncompressed **/Contents**
stream under *1 0 obj*.

**[missing_length.pdf](Stream_Length/Non-compressed/missing_length.pdf)** - This
file missing **/Length** key and is uncompressed. In general this PDF file is
not valid as it's hard to determine the correct size of stream. Even this fact,
PDF processors may render content in some level but rendered page content may be
incomplete or not shown at all.

**[missing_length_dl.pdf](Stream_Length/Non-compressed/missing_length_dl.pdf)** -
This file missing **/Length** as in previous example but contains **/DL** key
which points to decompressed size. As uncompressed streams have same **/Length**
and **/DL** (encrypted file exception) this may helps some PDF processor to
determine correct length of stream.

**[shorter_length.pdf](Stream_Length/Non-compressed/shorter_length.pdf)** - This
file has **/Length** specified shorter that is in reality. Different PDF
processors process this situation differently. Some shows part of content, some
nothing depepnding how they try to correct the situation.

**[shorter_length_dl.pdf](Stream_Length/Non-compressed/shorter_length_dl.pdf)** -
This is the same file as previous example but contains **/DL** key with
correct length.
