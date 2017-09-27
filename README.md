# MIDS - Medical Imaging Data Structure

Currently, distinc forms to store images and medical information exist, but there is not a standard that indicates how this information should be organized and shared. The BIMCV idea is to use a simple organisation that any researcher can understand the distribution of data.

This desing is called MIDS (Medical Imaging Data Structure). MIDS is a new standar that contains every type of medical information and images in simple hierarchy folders. This is born as an extension of the standard BIDS ([Brain Imaging Data Structure](http://bids.neuroimaging.io/),[1]). BIDS is a structure that collect medical brain images, but MIDS pretend to extend it far away and not limit it the use to medical brain images. the idea is to create the same structure with both brain, column images or torso,... whether Resonance magnetic, Computed tomography, ecography,... This structure will definitely follow the same process regardless of the type and shape of the image. 

In conclusion, MIDS gathers the essence of BIDS in terms of structure and naming but it is only defined in the case of brain images. MIDS aims to extend other anatomical parts following the same clear and easy structure of the BIDS

# Aplications
## XNAT2MIDS
This sorfware allow the user to Download one project into XNAT platform of BIMCV and convert the XNAT directory images in a directory MIDS. The aplication execution need Python --version >= 3.5. 

An example of execution is:

```sh
python3.5 main.py -w Project_id -i dirXNAT -o dirOutput
```

### Options

there are 3 funtions in this code:

  Download one project from xnat aplicatión:

     arguments:

      + Prefix	-p --project [PROJECT]	    1) The project name to download, if the project is omitted, the aplication show all projects in xnat to choice

      + Prefix	-i --input INPUT   	    2) the directory where the files will be downloaded
  
  Update the dictionary of scans, it is use to clasificate any medical image in MIDS structure:
  
      + Prefix  -c --csv    1)Scans dictionary is uploaded when this flag is appeared

  Convert the xnat directories of the project in MIDS format:

    arguments:

      + Prefix	-i --input INPUT	1) the directory where the files will be downloaded

      + Prefix	-o --output OUTPUT	2) Directory where the MIDS model is applied

# references

[1] Gorgolewski, K. J., Auer, T., Calhoun, V. D., Craddock, R. C., Das, S., Duff, E. P., ... & Handwerker, D. A. (2016). The brain imaging data structure, a format for organizing and describing outputs of neuroimaging experiments. Scientific Data, 3, 160044.
