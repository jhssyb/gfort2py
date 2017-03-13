![Build status](https://travis-ci.org/rjfarmer/gfort2py.svg?branch=master)

# gfort2py
Library to allow calling fortran code from python. Tested on python3, i think python2 mostly works except the unit tests. Requires gfortran>=6.0

## Build
````bash
ipython3 setup.py install --user
````

## Using

Compile code normnally (parsing -shared -fPIC as compile options to make a shared library at the end)

````python

import gfort2py as gf

SHARED_LIB_NAME='./test_mod.so'
MOD_FILE_NAME='tester.mod'

x=gf.fFort(SHARED_LIB_NAME,MOD_FILE_NAME)

````

x now contains all variables, parameters and functions from the module (tab completable)


## Testing

````bash
ipython3 setup.py tests
````

To run unit tests

## Things that work

### Module variables

- [x] Scalars
- [x] Parameters
- [x] Characters
- [x] Explicit size arrays
- [ ] Complex numbers
- [ ] Getting a pointer
- [ ] Assumed shape arrays
- [ ] Pointer/allocatable arrays
- [ ] Derived types
- [ ] Nested derived types
- [ ] Functions in derived types
- [ ] Other complicated derived type stuff (abstract etc)

### Functions/subroutines

- [ ] Basic calling
- [ ] Argument passing
- [ ] Argument intents
- [ ] Passing characters
- [ ] Optional arguments
- [ ] Keyword arguments
- [ ] Generic/Elemental functions
- [ ] Functions as an argument





