#get_functions

##Usage :
	get_functions [files_names]

Return all prototype of function found in the file.

*You can use like :* **get_functions *.c >> include.h**


##Examples :
	   get_functions bsq.c

###Return : 
	  char	      **get_map_from_file(char *str, int *nbr_lines);
	  int	      check_box_b(char **map, int xstart, int ystart, int len);
	  int	      check_box(int len, int largeur, char **map, int nbr_lines);
	  void	      make_something_for_me_bsq(char **map, int nbr_lines);
	  int	      main(int ac, char **av);
