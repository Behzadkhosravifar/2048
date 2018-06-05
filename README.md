## Mode

* Normal mode: 
[1×1](http://cyberzhg.github.io/2048/index.html?size=1) 
[2×2](http://cyberzhg.github.io/2048/index.html?size=2) 
[3×3](http://cyberzhg.github.io/2048/index.html?size=3) 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4) 
[5×5](http://cyberzhg.github.io/2048/index.html?size=5)
[6×6](http://cyberzhg.github.io/2048/index.html?size=6)
[7×7](http://cyberzhg.github.io/2048/index.html?size=7)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8)
* Auto move mode.
* Time rush mode.
* The new tile will always be 2: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=alwaysTwo) 
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=alwaysTwo)
* Fibonacci: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=fibonacci) 
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=fibonacci)
* Threes: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=threes)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=threes)
* Any two tiles can be merged: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=mergeAny)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=mergeAny)
* The new tile will be the power of 2: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=powerTwo)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=powerTwo)
* 0 is existed.
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=tileZero)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=tileZero)
* Negative numbers are existed.
[4×4](http://cyberzhg.github.io/2048/mode_negative.html)
* The tiles fall: 
[4×4](http://cyberzhg.github.io/2048/index.html?size=4&mode=gravity)
[8×8](http://cyberzhg.github.io/2048/index.html?size=8&mode=gravity)
* Auto flappy 2048:
[4×4](http://cyberzhg.github.io/2048/auto_flappy.html)

## Skin
* [死神永生](http://cyberzhg.github.io/2048/skin_santi.html)
* [使徒](http://cyberzhg.github.io/2048/skin_shito.html)
* [兵庫北](http://cyberzhg.github.io/2048/skin_bkb.html)
* [Chemical elements](http://cyberzhg.github.io/2048/skin_chemistry.html)


## Solve Puzzle by `javascript`

1. Open [Pazzle web page](http://cyberzhg.github.io/2048) by browser (like chrome)
2. Press F12 or devTools
3. Go to Console tab
4. Paste below codes
5. Press Enter to show step by step the best solution
6. Run again to go steps for `steps` times

#### By Display Mode:
```
var e = new Event("keydown");
var steps = 1000; // steps count
var go = function () {
    e.keyCode = Math.floor(Math.random() * 4) + 37;    
    e.which = e.keyCode;
    document.dispatchEvent(e);
    if (steps-- > 0)
        setTimeout(go, 10); // sleep 10 min second for every step
}
go();
```

#### Without Displaying and Faster:
```
var e = new Event("keydown");
var steps = 1000; // steps count
for(var i=0; i<steps; i++) {
    e.keyCode = Math.floor(Math.random() * 4) + 37;    
    e.which = e.keyCode;
    document.dispatchEvent(e);
}
```
