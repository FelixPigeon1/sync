```c
int main(void) {

}
```

Return type name of funciton(input of function) 

```c
double sum(double a, double b) {
	double res;
	res = a + b;
	return res;
}

int main(void) {
	double x = 5.1
	double y = 4.2
	double tot = sum(x,y);
	printf("tot = %f\n", tot);
	return 0;
}
```

Functions must be defined before they are called
Compiler must know what the function will look like
In order to not have to order the functions base on when they are first used, we can use prototype functions

```c
double sum(double, double);
```
this tells compiler that this function will exist with this format

functions can only return one thing
put function prototypes at the top
and actual functions at the bottom

c is always pass by value - makes a copy of what you pass in
sometimes its a value, 
changing x in a function will not change it outside the function
sometimes it can be a pointer,

to change a variable:
	pass a pointer
	function declaration must specify argument is a pointer

