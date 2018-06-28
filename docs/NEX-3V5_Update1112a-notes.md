# Notes on NEX-3V5_Update1112a

Firmware extraction done with [https://github.com/ma1co/fwtool.py](ma1co's fwtool.py).

## /0800_appli/usr/bin/app/main

### Interesting functions

    * sub_60199C : debug function, seems to be a printf-like function. Lots of cross-referencing to this function.
    * sub_63C958 : debug function, assert-like. Called with strings as arguments
    * sub_64FF0C : called with caller function name as arguments

### Interesting strings

    * MENU_ITEM_ID_MP4MP4_MOVIE_SIZE_720_FINE at 0xB8E701
