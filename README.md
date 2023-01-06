# lib-spwngen
A library for SPWN that lets you create levels with code, but lets you return the objects to a variable.

# Usage
```rs
let spwngen = import "lib.spwn";
spwngen.add({ OBJ_ID: 1, X: 15, Y: 15, GROUPS: 1g }) // Adds our object
spwngen.add(spwngen.move(1g, {
  X: 15,
  Y: 0,
  DURATION: 0.5
}));
let level = spwngen.export() // @array including all objects in level
let levelstring = spwngen.exportAsString() // returns the original levelstring
```
# But why?
This was made for the "isolates" concept, which is a concept where you can evaluate code in an isolated enviroment & get the resulting objects from the code. 

From there on, you will be able to return it to a variable or write it to a level.

I do not think that there are many uses for this, but if you do find a use, feel free to use this library.
