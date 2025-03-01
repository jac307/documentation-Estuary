
[Tutorials](../README.md) | [Tutorials in MiniTidal (TidalCycles), Hydra, & CineCer0](README.md)    

-------------------------------------------------------------------------------  

## CineCer0: Dynamic Values/Parameters

All functions that require a fixed numeric value can have a dynamic (animated) value instead. These are the two dynamic values/parameters you can use:

+ ramp
+ range

_________________________________________________________________________________________
_________________________________________________________________________________________

### ramp

+ `(ramp Dur_In_Cycles Initial_Value End_Value)` -- dynamic parameter that in # of cycles (time) goes from one value to the other

Ramp creates a dynamic (animated) value/parameter that goes from an initial value to a second value in an indicated time. This is a one way only animation.

#### Example 1:

In the following line of code, the size of the text is set to three times it size. This value is a fixed number = the text will just have this size until we change the value and re-evaluate the code.

+ `size 3 $ text "This is my text"`

If we replace the fixed value `3` for `(ramp Dur_In_Cycles Initial_Value End_Value)`, we will animate the size.

+ `size (ramp 3 1 5) $ text "This is my text"`

In the previous line of code, the size will run from size 1 to 5 in 3 cycles. By default, each cycle in Estuary is around 1 second.

<img src="imgs/cinecero-14.png" width="600">

#### Example 2:

In the following line of code, the coordinates are set to 0.5 in the X axis, and 0 in the Y axis. These are fixed values.

+ `setCoord 0.5 0 $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

If we replace the fixed value of `0.5` for `(ramp Dur_In_Cycles Initial_Value End_Value)`, we will animate the X coordinate.

+ `setCoord (ramp 8 (-0.5) 0.5) 0 $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

In the previous line of code, the X value will run from coordinate -0.5 (left) to 0.5 (right). This animation will happen in 8 cycles. The coordinate Y has a fixed value, therefore it won't change.

<img src="imgs/cinecero-15.png" width="600">

+ `setCoord (ramp 8 (-0.5) 0.5) (ramp 10 (-1) 1) $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

In the previous line of code, the Y value will also run from coordinate -1 (bottom) to 1 (top). This animation will happen in 10 cycles. In this case, both X and Y will be animated, moving from bottom-left to top-left.

<img src="imgs/cinecero-16.png" width="600">

_________________________________________________________________________________________
_________________________________________________________________________________________

### range

`(range Value_1 Value_2 $ sin Speed)` -- dynamic parameter that animates from one value to the other and viceversa with a # that determines the speed = parameters closer to 0 produce slower animations.

Range creates a dynamic (animated) value/parameter that comes and goes from one value to a second value in an indicated speed. This animation will go back and forward.

#### Example 1:

In the following line of code, the size of the text is set to three times it size. This value is a fixed number = the text will just have this size until we change the value and re-evaluate the code.

+ `size 3 $ text "This is my text"`

If we replace the fixed value `3` for `(range Value_1 Value_2 $ sin Speed)`, we will animate the size.

+ `size (range 3 1 $ sin 0.5) $ text "This is my text"`

In the previous line of code, the size will run back and forward from 1 to 5 with a speed of 0.5 --lower values on speed will go slower.

<img src="imgs/cinecero-17.png" width="600">

#### Example 2:

In the following line of code, the coordinates are set to 0.5 in the X axis, and 0 in the Y axis. These are fixed values.

+ `setCoord 0.5 0 $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

If we replace the fixed value of `0.5` for `(range Value_1 Value_2 $ sin Speed)`, we will animate the X coordinate.

+ `setCoord (range (-0.5) 0.5 $ sin 0.2) 0 $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

In the previous line of code, the coordinate X will run back and forward from -0.5 (left) to 0.5 (right) with a speed of 0.2. The coordinate Y has a fixed value, therefore it won't change.

<img src="imgs/cinecero-18.png" width="600">

+ `setCoord (range (-0.5) 0.5 $ sin 0.1) (range (-1) 1 $ sin 0.2) $ setSize 0.5 $ video "https://jac307.github.io/videoTextures/mariposa/01.mov"`

In the previous line of code, the coordinate Y will run back and forward from -1 (bottom) to 1 (top) with a speed of 0.1 --slower than the X dynamic value. In this case, both X and Y will be animated, moving back and forward.

<img src="imgs/cinecero-19.png" width="600">


--
