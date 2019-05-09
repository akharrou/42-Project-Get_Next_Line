# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: akharrou <akharrou@student.42.us.org>      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/02/17 16:23:01 by akharrou          #+#    #+#              #
#    Updated: 2019/05/08 18:03:27 by akharrou         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

CC          =	gcc
CFLAGS      =	-Wall -Wextra -Werror

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

NAME        =	libft.a

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

SRCS        =    ft_strchr.c                                \
                 ft_strjoin.c                               \
                 ft_strdup.c                                \
                 ft_strnew.c                                \
                 ft_strlen.c                                \
                 ft_strcat.c                                \
                 ft_memalloc.c                              \
                 ft_memset.c                                \

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

OBJS        =	$(SRCS:.c=.o)

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

all: $(NAME)

$(NAME): $(OBJS)
	@ar -rcs $(NAME) $(OBJS)
	@echo && echo $(GREEN) "[√]     [Library Successfully Compiled!]" && echo

%.o: %.c
	@$(CC) $(CFLAGS) -c $< -o $@
	@echo "Compiling => " $<

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

DEL = /bin/rm -rf

clean:
	@$(DEL) $(shell find . -name '*.o')

fclean: clean
	@$(DEL) $(NAME)

re: fclean all

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 

GREEN = "\033[1;32m"
WHITE = "\033[1;37m"

# — — — — — — — — — — — — — — — — — — — — — — — — — — — — — — 
