pyADS
=====

Python module to manipulate NTFS Alternate Data Stream (ADS) of files and directories in Python.

How it works?
-------------

On Windows Vista, Windows Server 2003 and later, NTFS Alternate Data Streams can be accessed using the
FindFirstStreamW and FindNextStreamW functions. So this module is a direct interface to this function
using ctypes and the kernel32 function.
The functionalities are:

* List streams
* Add a stream to a file
* Remove a stream from a file
* Read stream content

Class ADS
---------

All methods are grouped in an ADS class that allows multiple operations on the given file.

Fields are:

* **filename**: source file name for which streams are used
* **streams**: list of stream names

Methods are:

* **has_streams**: True if file has streams, ie `len(streams)>0`
* **add_stream_from_file**: add new stream from some file
* **delete_stream**: delete stream with given name
* **get_stream_content**: contents of the given stream


License
-------

This software is MIT-Licensed
