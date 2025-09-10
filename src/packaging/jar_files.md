# Jar Files

JAR files - short for **J**ava **Ar**chive - 
are just ZIP files with a few special bits of "metadata."

ZIP files are a common way of bundling a bunch of files up into one file.[^compression]

You don't need to know exactly where this metadata goes or what all of it is for yet,
just that at a high level it's all just files in a ZIP.

[^compression]: This bundling up also generally includes "compression," where
the single file might be smaller than the combined sizes of its components. Most people don't
need to think about this nowadays. Class files are small and hard drives are big.
I say that knowing full well that 145GB of the 500GB hard drive my work laptop is Baldurs Gate 3.
I have 4GB left.