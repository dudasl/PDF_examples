# PDF_examples
This project should collect various PDF examples files with various defects for
testing purposes.

## Stream_Length
This folder contains all PDF files where **/Length** key is broken (for example
missing, incorrect length, etc.)

**[correct_length.pdf](Stream_Length/Non-compressed/correct_length.pdf)** - This
is just reference file with correct **/Length** and uncompressed **/Contents**
stream under *7 0 obj*.

**[missing_length_1.pdf](Stream_Length/Non-compressed/missing_length_1.pdf)** - This
file missing **/Length** key and is uncompressed. In general this PDF file is
not valid as it's hard to determine the correct size of stream. Most PDF
processors are able to render content of the page without difficulties.
