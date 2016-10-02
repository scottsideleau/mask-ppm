#  mask-ppm
## Instructions for Generating and Viewing Masked PPM files

Generate a new Masked PPM file ("output.ppm"), taking an input image 
("image.ppm") and an image mask ("mask.pbm") as inputs.

A. Generate the masked PPM image to view.

  1. Open a terminal, navigate to your mask-ppm checkout, then type:

    ```bash
    bash mask.sh image.ppm mask.pbm > output.ppm
    ```

B. View the generated PPM image using command line tools.

  NOTE: These instructions assume a MacOS 10.11+ environment with Homebrew.
  
  1. Install a netpbm compatible image viewer (e.g. GraphicsMagick).

    ```bash
    brew cask install xquartz
    brew install graphicsmagick --with-x11
    ```

  2. Run XQuartz from Applications/Utilities/XQuartz and set the DISPLAY variable.

    ```bash
    export DISPLAY=:0
    ```

  3. Use the 'display' application from GraphicsMagick to view the image output.

    ```bash
    gm display output.ppm
    ```

C. Vew the generated PPM image using online tools.

  1. Open your favorite web browser (e.g. Google Chrome) and visit 
  [Netpbm Viewer](http://paulcuth.me.uk/netpbm-viewer).

  2. Drag-and-drop your output file ("output.ppm") into the web browser;
  specifically, taking care to drop it in the box labeled "Drag netpbm files
  here."
