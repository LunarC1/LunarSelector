## Statement
This library is used in combination with [LunarLib](https://github.com/LunarC1/Lunar)

## Installing and Running the Code
1. Download the code
2. Put "lunarselector/selector.h" in include folder
3. Put "lunarselector/selector.cpp" in src folder
4. Make sure to "#include "lunarselector/selector.h" at the top of main.cpp
5. Change the contents of your autonomous in the void statements in main.cpp
6. You're all set!

## Displaying custom images on the brain screen
1. Go to [LVGL Converter](https://lvgl.io/tools/imageconverter) and select LVGL V8
2. Select your image file (Can be .PNG.JPG)
3. Set color format to "CF_TRUE_COLOR_ALPHA" for transparent image support.
4. Set output format to "C array" (Should be default)
5. Hit the convert button
6. Go into the file and change line 12 from [#include "lvgl/lvgl.h"] to [#include "liblvgl/lvgl.h"]
7. Go to "lunarselector/selector.cpp" and add "LV_IMG_DECLARE(YOUR FILE/IMAGE NAME HERE);"
>[!IMPORTANT]
> Do NOT type out .c, only type out the file name.
8. Go to line 108 and add lv_img_set_src(YOUR FILE/IMAGE NAME HERE, &YOUR FILE/IMAGE NAME HERE); lv_obj_set_pos(YOUR FILE/IMAGE NAME HERE,0,0);
>[!IMPORTANT]
> Do NOT forget the & in the second parameter in lv_img_set_src.
> The second and third parameters are for X and Y coordinates on the screen

## Conclusion
Have fun with your custom brain screen!
Feel free to experiment around with it.

## FAQ
_**Is there support for Vexcode?**_
Currently, no. This project is PROS only.

_**I need help, where do I contact support?**_
Message nickson78181a on discord if you have any questions or want to contribute.
