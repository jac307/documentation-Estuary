
[Tutorials](../README.md) | [Tutorials on MiniTidal (TidalCycles), Hydra, & CineCer0](README.md)    

-------------------------------------------------------------------------------  


## MiniTidal: Transform Patterns

Once you have the basic structure (i.e. `s "bd cp*2"`), you can add transformations (after this structure) using the symbol `#`. This is the case for adding the `vowel` filter, changing the `gain`, adding panning (`pan`), changing pitch (`note`) and setting the sample number (`n`).  

Other types of transformations are added before this basic structure (i.e. `s "bd cp*2"`) using the symbol `$`. This is the case for `slow` and `fast`.  

We will review how to apply each of the above transformations.  

IMPORTANT: Be careful with the quotation marks you use. They must be this type `""`, not this type “” (they generate a syntax error). If you copy/paste code from this tutorial, make sure that it has the correct type since text-editing software often changes the style.

_________________________________________________________________________________________
_________________________________________________________________________________________

### Vowel Filter (`vowel`)

Play/hear the following:

+ `s "hh cp cp"`

Now try:

+ `s "hh cp cp" # vowel "a"`

3. The sound now has the filter `vowel` applied. The values for `vowel` are `a` `e` `i` `o` `u`

Try with the other values:

+ `s "hh cp cp" # vowel "e"`
+ `s "hh cp cp" # vowel "i"`
+ `s "hh cp cp" # vowel "o"`
+ `s "hh cp cp" # vowel "u"`

Now try with modifying the pattern:

+ `s "arpy cp arpy:2" # vowel "i"`
+ `s "sn sn:2 bd sn" # vowel "a"`
+ `s "[bd bd sn:5] [bd sn:3]" # vowel "e"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Changing the volume (`gain`) + Patterns in parameters

Play/hear the following:

+ `s "hh cp cp"`

Try:

+ `s "hh cp cp" # gain 0.5`

Try:

+ `s "hh cp cp" # gain 1.2`

The values for `gain` are numbers from `0` (no sound) to `2.0` (the loudest it can get). Be careful with values higher that `1.5`.

The above examples have a single value, but you can also add multiple values.  

Try:

+ `s "hh cp cp" # gain "0.5 1.1 0.8"`

You can see that each of the three samples have different volumes. This is because gain is now a pattern (using values in between quotation marks) with three values.  

Try this other example:

+ `s "hh cp cp" # gain "0.5 1.1"`

Now, it is only two values with three samples. The gain pattern will start with the sound pattern, but then it will deviate since it is repeating sooner.  

IMPORTANT: For these patterns to work on the transformations, you must have the same or a higher amount of samples in the `s` patterns.  

Now try with more variations:

+ `s "arpy cp arpy:2" # gain "0.2 1 0.8”`
+ `s "sn sn:2 bd sn" # gain "0.5 1.1 0.8 0.4”`
+ `s "[bd bd sn:5] [bd sn:3]" # gain "0.5 1.1"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Panning (`pan`)

Use headphones!  

Play/hear the following:

+ `s "hh cp cp"`

Try the following lines separately:

+ `s "hh cp cp" # pan 0`
+ `s "hh cp cp" # pan 0.5`
+ `s "hh cp cp" # pan 1`

Values for `pan` go from `0` (sound totally on the left channel) to `1` (sound totally on the right channel).  

You can also use patterns with the `pan` parameters:

+ `s "hh cp cp" # pan "0 0.5 1"`
+ `s "arpy cp arpy:2" # gain "0 1"`
+ `s "sn sn:2 bd sn" # gain "0.5 0.2 0.8 1"`
+ `s "[bd bd sn:5] [bd sn:3]" # gain "0.2 0.8"`

_________________________________________________________________________________________
_________________________________________________________________________________________

### Sample Number (`n`) + dynamic parameters

Play/hear the following:

+ `s "hh cp cp"`

Now try the following lines separately:

+ `s "hh cp cp" # n 1`
+ `s "hh cp cp" # n 3`

`n` is similar to using `s "hh:1 cp:1 cp:1"` but helps applying the selection of the sound file to all of the samples. Values of `n` start with `0` (default: first file).  

You can use the dynamic value `(choose[])` to generate more random variations.  

Try this example:

+ `s "hh cp cp" # n (choose[0,3,2])`

Now, the value of `n` is randomly chosen from the list of values we wrote inside `[]`.  

Another dynamic value that we can use is `(irand)` that will give us a random number between `0` and the value we add after the function `irand`.  

Try this example:

+ `s "hh cp cp" # n (irand 4)`

The value of `n` is randomly chosen from the first `5` sound files (remember we are counting from `0`!) of each of the samples.  

Try with more variations:

+ `s "arpy cp arpy" # n (irand 2)`
+ `s "sn sn bd sn" # n (irand 3)`


_________________________________________________________________________________________
_________________________________________________________________________________________

### Modify the time of the pattern (`slow` and `fast`)

Play/hear the following:

+ `s "hh cp cp"`

Now try:

+ `slow 2 $ s "hh cp cp”`
+ `fast 2 $ s "hh cp cp"`

`slow` slows the time of the pattern, while `fast` do the opposite. Parameters for both cases start from `1` (default) and grow from there (it can also go lower). They cannot be used at the same time.  

Try with more variations:

+ `slow 1.3 $ s "arpy cp arpy:2"`
+ `fast 5 $ s "sn sn:2 bd sn"`
+ `slow 2 $ s "[bd bd sn:5] [bd sn:3]"`


_________________________________________________________________________________________
_________________________________________________________________________________________

### Multiple Transformation

You can mix and match all of the above!

+ `s "drum drum drum drum" # vowel "a o e e" # gain 1.2`
+ `fast 2 $ s "bd hh sn:1 hh sn:1 hh" # gain "1 0.7 0.5" # pan (choose[0,1])`
+ `slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a"`
+ `s "drum ~ drum drum" # n (choose [0,2,3]) # gain (choose[1, 1.2,0.8])`

Experiment!

_________________________________________________________________________________________
_________________________________________________________________________________________

### Multiple Sound Patterns

+ You can play multiple sound patterns using the following structure:  

`stack [
s "drum drum drum drum" # vowel "a o e e" # gain 1.2,
fast 2 $ s "bd hh sn:1 hh sn:1 hh" # gain "1 0.7 0.5" # pan (choose[0,1])
 ]`  

You can add more sound patterns. Just end each one with a `,` (comma) at the end of each. All patterns should be inside `stack []`. The last sound pattern should not have a comma.  

+ Play the following:  

`stack [
s "drum drum drum drum" # vowel "a o e e" # gain 1.2,
slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a",
slow 2 $ s "numbers:1 numbers:2 numbers:3 numbers:4" # pan "0 0.5 1" # vowel "a",
s "drum ~ drum drum" # n (choose [0,2,3]) # gain (choose[1, 1.2,0.8])
]`

+ Play around!  

Part of live coding practices is improvising: changing values and adding transformations on the go, constantly playing what you modify.
