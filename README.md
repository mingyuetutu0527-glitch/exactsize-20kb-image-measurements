# ExactSize 20 KB Image Output Measurements

Reusable measurements showing how much image content fits within a 20 KiB
(20,480-byte) JPEG budget. The dataset contains six fixed input images
compressed with the ExactSize browser tool, with output dimensions, byte counts,
pixel counts, bytes per pixel, and encoder quality.

The data is useful for interface copy, file-upload validation, and rough
capacity planning. It is not a predictive distribution: each content type has
one sample, and browser encoders and individual images can differ.

## Files

| File | Contents |
| --- | --- |
| `data/20kb-image-output-measurements.csv` | Six source-to-output measurements at a 20 KiB target |
| `docs/methodology.md` | Scope, definitions, collection method, and limitations |

## Method at a glance

Measurements were collected on 18 October 2026 in Chrome 155.0.8059.80 on
Windows 11. Each fixed source image was compressed once as JPEG at a target of
20 KiB using the ExactSize tool. The output dimensions, byte count and reported
quality were recorded without a further re-encode. The compressor reduces
quality no lower than 40%; after that it reduces pixel dimensions.

For the complete context, source descriptions, and additional format
comparisons, see the [ExactSize 20 KB measurement page](https://crunchimage.com/compress-image-to-20kb).
