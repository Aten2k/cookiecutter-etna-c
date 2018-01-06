CC	= gcc
CFLAGS	= -Wall -Wextra -Werror -pedantic
OBJ	= $(SRC:.c=.o)

SRC	= 
RM	= rm -rf
NAME	= {{cookiecutter.project_name|lower}}


.PHONY: all clean fclean re

all: $(NAME)

clean:
	$(RM) $(OBJ)

fclean: clean
	$(RM) $(NAME)

re: fclean all
