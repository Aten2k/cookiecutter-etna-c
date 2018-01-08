##
## Makefile for {{cookiecutter.project_name|lower}} in /home/work/{{cookiecutter.project_name}}
##
## Made by {{cookiecutter.full_name}}
## Login   <{{cookiecutter.email}}>
##
## Started on  Fri Nov  10 21:33:56 2017 {{cookiecutter.full_name}}
## Last update Fri Nov  10 21:33:56 2017 {{cookiecutter.full_name}}
##

CC          =   gcc
CFLAGS      =   -W -Wall -Werror -pedantic -Iincludes
RM          =   rm -f
NAME        =   {{cookiecutter.project_name|lower}}
SRC			=	src/{{cookiecutter.project_name|lower}}.c


OBJ     = $(SRC:.c=.o)

$(NAME) : $(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(NAME)

debug   : $(OBJ)
	$(CC) $(CFLAGS) -g3 $(OBJ) -o $(NAME)

all     : $(NAME)

clean   :
	$(RM) $(OBJ)

fclean  : clean
	$(RM) $(NAME)

.PHONY  : clean debug fclean all

