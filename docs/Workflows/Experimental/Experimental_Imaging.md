# Imaging

You can image with whatever technology suits your project best. In general most people use:

## Imaging modalities

- H&E: Quick, simple, cheap, and pathology friendly
- IHC: Targeted with antibody, does not require fluoresence
- IF: Targeted with antibodies, a single round can have up to 5 stains.
- mIF: IF with manual handling between cycles

### H&E

- Fast, cheap, and standard for pathologists world-wide
- Many deep learning models exist to predict features
- Fast to stain tissue, fast to image tissue

### Immunohistochemistry

- Antibody-based + enzymatic dying
- Brightfield imaging, therefore fast and low-storage cost.

### Immunofluorescence

- Antibody-based
- Panel design is important to ensure that signal spillover is minimal

Note: Here you should consider creating calibration points by etching the membrane with the LMD.

### Multiplex Immunofluorescence

Note: Here you should consider creating calibration points by etching the membrane with the LMD.

## Microscopes and critical settings

Microscopes vary plenty

### Magnification

- 10X good enough for FlashDVP ROI manual annotation (not single cells).
- 20X minimum for image analysis driven DVP or single cell manual annotations.
- 40X and above: Allows for more granular morphological and more detailed cell-based analysis.

### Binning

- 1x1 binning, highest resolution, largest file sizes
- 2x2 binning: half the resolution, 1/4 the file size, higher signal-to-noise ration

### File formats

If you plan to just perform manual annotations, your bottlenect is getting your image into QuPath.  
QuPath can take in a large variety of formats, please consult the [Bioformats Compatibility Table](https://docs.openmicroscopy.org/bio-formats/5.8.2/supported-formats.html).

If you plan to perform image-analysis, ensure that your software solution can digest the file format. Perhaps consult your friendly image analyst for clarification.
