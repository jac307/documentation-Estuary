
[Tutorials](../Tutorials/README.md) | [Tutorials in MiniTidal (TidalCycles), Hydra, & CineCer0](README.md)    

-------------------------------------------------------------------------------  

## MiniTidal: Cheatsheet

### Basic Sonic Patterns

+ `s "sound"` -- single sound each cycle
+ `s "sound sound"` -- two sounds each cycle
+ `s "sound*4"` --one sound playing 4 times each cycle
+ `s "sound:2"`--accessing the file no.2 of a sample
+ `s "<sound sound>"` --each cycle will have a different sound
+ `s "[sound sound] sound"` -- first half of the cycle plays two sounds (faster), second half plays one sound (slower)
+ `s "[sound sound]/3 sound"` --first half of the cycle plays two sounds but the time is divided so it is perceived slower.

### Functions-Transformations applied "before" the Sonic Pattern

+ `slow 1 $` -- slow the cycle, 1 is the default. 1++ = slower.
+ `fast 1 $` -- fast the cycle, 1 is the default. 1++ = faster.
+ `chop 8 $` -- cuts the samples a # of times.
+ `striate 8 $` -- granulates the sound.
+ `degrade $` -- randomly removes events from the sonic pattern.
+ `rev $` -- returns a reverse version of the sonic pattern.
+ `jux ([transformation]) $` -- creates strange stereo effect by applying a function-transformation.
+ `every 2 ([transformation]) $` -- applies a function-transformation every # of cycles.
+ `always ([transformation]) $` -- applies a function-transformation a certain % of times. Other possible parameters: `almostAlways`, `often`, `sometimes`, and `rarely`.

### Functions-Transformations applied "after" the Sonic Pattern

+ `# gain 1` -- changes the volume of the sound; 1 = normal vol, 1-- = less volume, 1++ = more volume (even if the value is higher, it does not exceed 2 as a save value).
+ `# n 0` -- changes the number of the sample.
+ `# note 0` -- changes the note.
+ `# speed 0` -- changes the speed; 1 = normal speed.
+ `# pan 0.5` -- moves the sound on the speakers; 1 = right, 0 = left
+ `# vowel "a"` -- applies a filter; other values: `e`, `i`, `o`, `u`
+ `# shape 5` -- produces a wave shaping distortion; 0 = no distortion.
+ `# accelerate 2` -- similar to speed.
+ `# begin 0.1` -- cuts the beginning of the samples
+ `# end 0.9` -- cuts the ending of the samples

### Dynamic Parameters

+ `"1 2 3 4"` -- a parameter pattern, it only works completely when the sound pattern has the same or more amount of values.
+ `(choose[1,2,3,4])` --parameter chose from the list in order
+ `(irand 5)` -- parameter oscilantes between 0 to the value you give
+ `(rand + 0.5)` -- parameter oscilantes between 0 and 1 + the value you give; in this example, it between 0.5 and 1.5

### Multiple Statements

`stack[
statement-1,
statement-2
]`






-
