# parse_file

------------------------------------------------------------------------
## UPDATE 1
Add optionnal option for automatically include header in div file.

## UPDATE 2
Change /*Title*/ by /*@Title*/.

### Example
	parse_file main.c -i 'one,two'

### Output file
```c
/*
** main.c for toto in /home/oom/Documents/Temp
**
** Made by oom
** Login   <oom@epitech.net>
**
** Started on  Thu Feb 19 10:04:06 2015 oom
   Last update Thu Apr 30 00:56:18 2015 schweitzer lucas
*/

#include "one.h"
#include "two.h"

int     main(int ac, char **av)
{
  print_char('%');
  print_str("test");
  return (0);
}
```
------------------------------------------------------------------------
## Usage 
	parse_file [file_to_cut]

Parse one file in multiple file for respect the Epitech's norm and return the name of files for pastle in Makefile.

The parsing pastle the functions without the includes.

*You can use like :* **parse_file main.c**

## Example
	parse_file main.c
### Content of main.c
```c
/*
** main.c for toto in /home/oom/Documents/Temp
**
** Made    by oom
** Login   <oom@epitech.net>
**
** Started on  Thu Feb 19 10:04:06 2015 oom
** Last update Thu Feb 19 10:20:22 2015 oom
*/

/*@Utils*/
int	get_strlen(char *str)
{
  int	i;

  i = 0;
  while (str[i])
      i++;
  return (i);
}

/*@Print*/
void	print_char(char c)
{
  write(1, &c, 1);
}

void	print_str(char *str)
{
  write(1, &str, get_strlen(str));
}

/*@Main*/
int	main(int ac, char **av)
{
  print_char('%');
  print_str("test");
  return (0);
}
```      

### Return  
	utils.c \
	print.c \
	main.c


### In utils.c
```c
/*
** utils.c for toto in /home/oom/Documents/Temp
**
** Made by oom
** Login   <oom@epitech.net>
**
** Started on  Thu Feb 19 10:04:06 2015 oom
** Last update Thu Feb 19 10:09:00 2015 oom
*/

int	get_strlen(char *str)
{
  int	i;

  i = 0;
  while (str[i])
    i++;
  return (i);
}
```

### In print.c
```c
/*
** print.c for toto in /home/oom/Documents/Temp
**
** Made by oom
** Login   <oom@epitech.net>
**
** Started on  Thu Feb 19 10:04:06 2015 oom
** Last update Thu Feb 19 10:09:00 2015 oom
*/

void	print_char(char c)
{
  write(1, &c, 1);
}

void	print_str(char *str)
{
  write(1, &str, get_strlen(str));
}
```

### In main.c 
```c
/*
** main.c for toto in /home/oom/Documents/Temp
**
** Made by oom
** Login   <oom@epitech.net>
**
** Started on  Thu Feb 19 10:04:06 2015 oom
** Last update Thu Feb 19 10:09:00 2015 oom
*/

int	main(int ac, char **av)
{
  print_char('%');
  print_str("test");
  return (0);
}
```

