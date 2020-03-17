

# _Printf in c

***Description*** 📋

This project is about making our own printf function in C programming languaje , it was faced in a critical and challenge way.

> Use git clone to get our code in your local machine and see how it works.

```bash
git clone https://github.com/JoseR98/printf.git
```

##  Testing cases. ⚙️

```python
_printf(NULL);
	printf(NULL);
	printf("--------------------------\n");
	printf("Testing %% without formats\n");
	printf("--------------------------\n\n");
	
	_printf("Own printf: %%\n");
	printf("Original printf: %%\n");
	printf("--------------------------\n");
	
	printf("Own printf:\n");
	_printf("hola%");
	_printf("\n1");
	_printf("\b3");
	_printf("\f4");
	_printf("\r5");
	_printf("\t6");
	_printf("\v7");
	printf("Original printf:\n");
	printf("hola%");
	printf("\n1");
	printf("\b3");
	printf("\f4");
	printf("\r5");
	printf("\t6");
	printf("\v7");
	printf("--------------------\n");
	_printf("Own printf: %");
	printf("\nOriginal printf: %");*/
	printf("--------------------------\n");
	_printf("Own printf: %%%zhola; ");
	printf("Original printf: %%%zhola");
	printf("\n--------------------------\n");
	_printf("Own printf: %%%z\n");
	printf("Original printf: %%%z\n");

```

## Holberton task 💎

##### ◉ Task 0

Write a function that produces output according to a format.

- ###### *c*

- ###### *s*

**Functions  prototype** ⬇︎

```c
int fn_string(va_list s);
int fn_char(va_list c);
```

```c
void main()
{
	_printf("=============\n");
	_printf("TESTING CASES\n");
	_printf("=============\n\n");
	char *greeting = "Hello Dude !";
	printf("-------Say hi---------\n");
	_printf("Own printf is greeting: -> %s\n", greeting );
	printf("Original printf greeting: -> %s\n", greeting );
  int holbi = 'H';
	_printf("Holberton first Letter: -> %c \n ", holbi );
	printf("Holberton first Letter: -> %c \n ", holbi );
}
```

**Output** 🛠

```CQL
=============
TESTING CASES
=============

-------Say hi---------
Own printf is greeting: -> Hello Dude ! 
Original printf greeting: -> Hello Dude ! 
Holberton first Letter: -> H 
Holberton first Letter: -> H 
```



##### ◉Task 1

Handle the following conversion specifiers:

- ###### *d*

- ###### *i*

**Function  prototype ** ⬇︎

```c
int fn_int(va_list args);
```

```c
void main()
{
	_printf("=============\n");
	_printf("TESTING CASES\n");
	_printf("=============\n\n");	
	int year = 1917;
	_printf("-------¿Year Betty's birthday?---------\n");
	_printf("Own printf which is betty's year birthday ?: -> %d \n ", year );
	printf("Original printf which is betty's year birthday?: -> %d \n ", year );
  
  _printf("=============\n");
	_printf("TESTING CASES\n");
	_printf("=============\n\n");	
	int actualYear = 2020;
	_printf("-------¿Actual year?---------\n");
	_printf("Own printf actual year?: -> %i \n ", actualYear );
	printf("Original printf actual year?: -> %i \n ", actualYear );

}
```

***ouput***  🛠

```CQL
=============
TESTING CASES
=============

-------¿Year Bettys birthday?---------
Own printf which is bettys year birthday ?: -> 1917 
 Original printf which is bettys year birthday?: -> 1917 
```

```CQL
-------¿Actual year?---------
Own printf actual year?: -> 2020 
 Original printf actual year?: -> 2020 
```



##### ◉Task 3

- *b*

**Function prototype** ⬇︎

```c
int fn_bin(va_list args);
```

```c
void main()
{
	_printf("=============\n");
	_printf("TESTING CASES\n");
	_printf("=============\n\n");	
	_printf("%b\n", 98);

}
```

***Output*** 🛠

```CQL
=============
TESTING CASES
=============

1100010
```



##### ◉Task 4

Handle the following conversion specifiers:

- *u*

- *o*

- *x*

- *X*

  

  **Function prototypes** ⬇︎

```c
int fn_octal(va_list num);
int fn_un(va_list args);
int fn_Hexa(va_list args);
int fn_hexa(va_list args);
```

```c
void main()
{
	_printf("=============\n");
	_printf("TESTING CASES\n");
	_printf("=============\n\n");	

	unsigned int ui;
	ui = (unsigned int)INT_MAX + 1024;

	_printf("Own printf -> Unsigned octal: -> [%o]\n", ui);
  printf("Original printf Unsigned octal:[%o]\n", ui);
  _printf("Own printf -> Unsigned hexadecimal:[%x, %X]\n", ui, ui);
  printf("Original printf Unsigned hexadecimal:[%x, %X]\n", ui, ui);
	

}
```

***Output*** 🛠

```CQL
=============
TESTING CASES
=============

Own printf -> Unsigned octal: -> [20000001777]
Original printf Unsigned octal:[20000001777]
Own printf -> Unsigned hexadecimal:[800003ff, 800003FF]
Original printf Unsigned hexadecimal:[800003ff, 800003FF]
```



##### ◉Task 14

Handle the following custom conversion specifier:

- ***r***

  

  **Function prototype**

  ```c
  int fn_bin(va_list args)
  ```

  ```c
  void main()
  {
  	_printf("=============\n");
  	_printf("TESTING CASES\n");
  	_printf("=============\n\n");	
  
  	char *reverstring = "Holberton";
    
  	_printf("-------Reversing a string---------\n");
  	_printf("Own printf -> Reversing string: -> [%r]\n", reverstring);
  
  }
  ```

  **Output** 🛠

  ```CQL
  =============
  TESTING CASES
  =============
  
  -------Reversing a string---------
  Own printf -> Reversing string: -> [notrebloH]
  ```

  

  ##### ◉Task 15

  Handle the following custom conversion specifier:

  - ***R***

  

  ​	**Function prototype**

  ```c
  int fn_rot13(va_list args);
  ```

  ```c
  void main()
  {
  _printf("=============\n");
  _printf("TESTING CASES\n");
  _printf("=============\n\n");	
  
  char *root13 = "H0lb3rt0n 5ch00l";
    
  _printf("------- ROOT 13---------\n");
  _printf("Own printf -> ROOT 13: -> [%R]\n", root13);
  }
  ```

  **Output**  🛠

  ```CQL
  =============
  TESTING CASES
  =============
  
  ------- ROOT 13---------
  Own printf -> ROOT 13: -> [U0yo3eg0a 5pu00y]
  ```

  

  

  

  👨🏻‍💻 Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

  **Developed by**: 

  **Jose Alonso Restrepo** -  *GitHub user* ➞ 🖥 [JoseR98](https://github.com/JoseR98)                                                     

  **Juan Sebastian Bueno** - *GitHub user* ➞ 🖥  [sebastianbm9507](https://github.com/sebastianbm9507)     
  
  **March 17 2020**

  

  

  ​	

  

  

  

  
