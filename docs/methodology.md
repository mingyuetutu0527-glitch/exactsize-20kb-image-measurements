# Methodology and limitations

## Collection

Every row records a run of the ExactSize compressor on 18 October 2026. The
operator loaded one fixed test image, selected JPEG output, set a 20 KiB target
(20,480 bytes), ran compression, and copied the tool's output dimensions, byte
count and JPEG quality. No output was encoded again after the tool completed.

The environment was Chrome 155.0.8059.80 on Windows 11. Canvas encoder output
can differ across browser engines, so the last digit of a byte count should be
treated as environment-specific.

## Definitions

`bytes_per_pixel` is `output_bytes / (output_width_px * output_height_px)`.
`output_megapixels` is the output pixel count divided by 1,000,000 and rounded
to two decimal places in the table. The reported target is a binary kibibyte
value: 20 KiB = 20 × 1,024 = 20,480 bytes.

## Scope

There are six samples, one for each content type. They demonstrate that a fixed
byte budget behaves differently for photographs, text, flat graphics,
gradients, and transparency. They are not estimates of the spread within any
content type and must not be used as a guarantee for an arbitrary image.

The compressor will not reduce JPEG quality below 40%. Once that floor is
reached, it reduces output dimensions instead. This rule materially affects all
rows in this dataset.
