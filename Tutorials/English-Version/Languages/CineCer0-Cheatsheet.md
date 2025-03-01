
[Tutoriales](../README.md) | [Tutoriales en MiniTidal (TidalCycles), Hydra, y CineCer0](README.md)    

-------------------------------------------------------------------------------  

## CineCer0: Cheatsheet

### Playing Videos, Images, or Text

+ `video "videoURL"`
+ `image "imageURL"`
+ `text "This is not a text"` -- what you have inside quotation marks is the text that will appear.

###  Parameters: Fixed Numbers

+ Negative numbers must be inside parentheses `()`.
+ Positive numbers can be without parentheses.

###  Position on Videos, Images, or Text

+ `setPosX x $` -- from left (-1) to right 1
+ `setPosY y $` -- from bottom (-1) to top 1
+ `setCoord x y $`

###  Videos with Audio

+ `vol 0.5 $` -- no vol 0 to max vol 1

###  Video/Image functions

+ `setWidth w $` -- 1 = natural width
+ `setHeight h $` -- 1 = natural height
+ `setSize wh $` --one value will affect proportionally the width and height
+ `setRotate d $` --value in grades
+ `setOpacity o $` -- from 0 to 1 (no opacity)
+ `setBlur bl $` -- 0 = no blur (1++ = more)
+ `setBrightness br $` -- 0-0.9 = less, 1++ = more
+ `setContrast c $` -- 0-0.9 = less, 1++ = more
+ `setGrayscale g $` -- 0 = color, 1 = to grayscale
+ `setSaturate s $` -- 1 = natural saturation (1++ = more, 1-- = less)
+ `circleMask m $` -- 0 no mask, 0-0.99 bigger mask (growing from the centre)
+ `circleMask' m x y $` -- similar to circleMask but with a third value that affects the position of the mask in the centre
+ `sqrMask m $` -- 0 no mask, 0-0.99 bigger mask ((growing from the centre)
+ `rectMask t r b l $` -- four values: top, right, bottom, left.
+ `z n $` -- change in the order of the layer

###  Text Function

+ `size n $` -- 1++ bigger font size
+ `font "fontType" $` -- change font, name must be inside quotation marks; *use only [safe web fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php){:target="_blank"}
+ `colour "colour" $` -- change colour, value = hexacolor --must be inside quotation marks
+ `rgb r g b $` -- change colour, values = red green blue, normalized from 0 to 1
+ `rgba r g b a $` -- with fourth value = alpha
+ `hsl h s l $` -- change colour, values = hue saturation lightness, normalized from 0 to 1
+ `hsla h s l a $` -- with fourth value = alpha
+ `strike $` -- crossed text
+ `bold $` -- bold text
+ `italic $` -- italic text
+ `z n $` -- change in the order of the layer

###  Dinamic Parameters

+ `(ramp Dur_In_Cycles Initial_Value End_Value)` -- dynamic parameter that in # of cycles (time) goes from one value to the other
+ `(range Value_1 Value_2 $ sin Speed)` -- dynamic parameter that animates from one value to the other and viceversa with a # that determines the speed = parameters closer to 0 produce slower animations.


-
