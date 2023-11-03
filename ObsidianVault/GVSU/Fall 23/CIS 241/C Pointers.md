`%` = memory address


```c
int *p1 = (int *) malloc(sizeof(int)*7);
int *p2 = (int *) malloc(sizeof(int)*7);
```

assigns the memory needed for 7 integers to

p1 points to 1e0 in the memory address

(integers are 4 bytes, addresses in memory will increase by 4 for every int allocated)

p2 points to 20e

p1+n access elements into that array
if n goes above the array size it can start to access parts of memory beyond the array size causing issues that are a pain to detect

p2 = p3 causes a memory leak if p2 is not freed before the reassignment
p2 will also point to p3 leaving that allocated memory behind

call `free()` for the first block of memory (p1, no plus or minus)

