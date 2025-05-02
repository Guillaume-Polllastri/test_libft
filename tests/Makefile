# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gpollast <gpollast@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2025/04/27 21:14:10 by gpollast          #+#    #+#              #
#    Updated: 2025/04/30 18:28:54 by gpollast         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC = gcc
CFLAGS = -Wall -Werror -Wextra -I..
LDFLAGS = -L.. -lft -lbsd
TARGET = a.out
MAKE = make
SRCS = main.c
OBJS = $(SRCS:.c=.o)
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@
all: $(OBJS)
	$(CC) $(OBJS) $(LDFLAGS) -o $(TARGET)
clean:
	rm -f $(OBJS)
fclean: clean
	rm -f $(TARGET)
re: fclean all

test: all 
	make -C .. && ./a.out
.PHONY: all clean fclean re test
