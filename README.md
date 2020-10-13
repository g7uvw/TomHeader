# TomHeader
The TOM file format is used by the MuCAT series of XMT scanners at QMUL. It is a 512 byte header as specified in the tomheader.h file. The TOM format is supported by Drishti (https://github.com/nci/drishti) and TomView (http://qmxmt.com/scans/Tomview/)

The first three 16bit words of the header (xsize,ysize,zsize) specify the X, Y and Z dimentions of the 3D volume contained in the file. As a quick check of file integrity, the filesize should be equal to xsize x ysize x zsize + 512 bytes. The 3D volume data starts directly after the header and is composed of zsize number of xsize x ysize uncompressed 8bit integer greyscale bitmaps.  

TomView can produce a macro to import a TOM file into ImageJ for further analysis or to allow conversion to other formats.
