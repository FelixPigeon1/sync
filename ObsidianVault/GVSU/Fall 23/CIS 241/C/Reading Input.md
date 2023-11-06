## Reading From STDIN

```c
int main(void) {
	int x = 5;
	printf("x = %d\n", x);
	return 0;
}
```

Prints the value of x

```c
int main(void) {
	int a, b, c;
	scanf("%d %d %d", &a, &b, &c);
	tot = a+b+c;
	printf("tot = %d\n", tot);
	return 0;
}
```

Look for an input that matches the quotes and put those values at those memory addresses

```c
int main(void) {
	int num;
	int sum = 0;

	while (ret != EOF) {
		printf("current sum = &d/n", sum);
		scanf("%d", &num);
		sum += num;
	}
}
```

Reads input from STDIN until the EOF signal is sent (Ctrl-D)

```c
int main(void) {
	int num;
	int sum = 0;

	while (ret != EOF) {
		printf("current sum = &d/n", sum);
		ret = scanf("%d", &num);
		sum += num;
	}
}
```

```scanf``` returns 0 or -1 depending on the implementation when the EOF signal is sent
Only use scanf if its well structured


```c
int main(void) {
	int maxn = 10;
	char *p = (char *) malloc(sizeof(char)+maxn);
	p = fgets(p, maxn, stdin);
	if (p != NULL) {
		printf("you entered %s\n", p);
	}
	return 0;
}
```

This limits the amount of memory that gets assigned to the memory address of p
in this case it allocated the amount required for p up to a max of 10
Always include checks in your c code to catch errors in built in functions


```c
int main(void) {
	char *s
	size_t maxn = 10;
	s = (char *) malloc(sizeof(char)*maxn);
	getline(&s, &maxn, stdin);
	printf("you entered: %\n", s);
	printf("maxn = %d/n", maxn);
	return 0;
}
```

getline (address of pointer, )
does something idk
maxn - the max bytes that could be allocated, but not the total that *is* allocated

