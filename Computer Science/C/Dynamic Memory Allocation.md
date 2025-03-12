# `malloc()`
- Syntax:
	- ```c
	  malloc(n*sizeof(dataype));
	  ```
- Returns a pointer which allocates a continous memory location of size `n` which is the argument passed.
- After allocation, `malloc()` does not initialize the value of the location.
- `malloc()` is faster than `calloc()` because it is continous <font color=red>(what logic)</font> 
# `calloc()`
- Syntax:
	- ```c
	  calloc(n,sizeof(datatype));
	  ```
- Returns a pointer which will allocate blocks of locations
	- (maybe) check for `n` blocks where `n` is the first parameter, each of size `s`(secong parameter). The end of one block points to the start of the next.
- After allocation, `calloc()` will initialize the value of location to be `0`.
- `calloc()` is (maybe) faster than `malloc()` because it has to search for block (an maybe store pointer)(address of next block in current block).

# Others
- There are also `free()` and `realloc()` commands.