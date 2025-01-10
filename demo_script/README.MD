# Demo script for comparison of Dec-Tiff, Cpp-Tiff, Tifffile, Libtif

## Prerequisites for the demo

```
pip install tifffile
pip install libtiff
pip install cpp-tiff
```

To achieve optimal performance, it is recommended to clear disk fragments before downloading the test data. 

## Demo run

Set type to change the test tools. To avoid the impact of CPU cache, run RAMMap64.exe, click Empty->Empty Standby List after each test.

Test data load : compare_load.py

Test data save : compare_save.py