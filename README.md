# PHYS5011BrownianMotion

What we need to do

Import .tif files for each of the 3 test runs for each of the 4 substrates with varying sizes of polystyrene beads

Need to take each slide (~167/sample) and switch to greyscale

Once in greyscale, need to normalize the background to zero,( aka remove shadows)

We should then be able to take our image data and turn it into a matrix where the background is normalized to zero and the observable polystyrene beads are some value greater than zero.

We will have a matrix for each of the 167 slides for each of the 3 runs for each of the 4 samples, this will allow us to trace the movement of the polystyrene beads through the 167 slides,,

We should then be able to export the data,

Since we are uploading 3 tests for 4 different samples , we upload 12 PowerPoints (.tiff), we should get 12 files back with the matrix movement, 

What file type do we want back? Csv? If csv, we will then have to create a program to tell us the Brownian motion of each bead.


File organization on my desktop
*might be helpful for readjusting to run code on another system*

Users
└── kalibyrnes
└── Desktop
└── Fall2025
└── PHYS5011
└── BrownianMotion
└── Data
├── 4.11μm
│   ├── 4.11μmTake1.tif
│   ├── 4.11μmTake2.tif
│   └── 4.11μmTake3.tif
├── 950nm
│   ├── 950nmTake1.tif
│   ├── 950nmTake2.tif
│   └── 950nmTake3.tif
├── 752nm
│   ├── 752nmTake1.tif
│   ├── 752nmTake2.tif
│   └── 752nmTake3.tif
└── 535nm
    ├── 535nmTake1.tif
    ├── 535nmTake2.tif
    └── 535nmTake3.tif
