NAME = phonebook

SRCS = PhoneBook.cpp \
       Contact.cpp \
       main.cpp

OBJS = $(SRCS:.cpp=.o)
D_FILE = $(SRCS:.cpp=.d)

CXX = g++
CXX_FLAGS = -Wall -Wextra -Werror -std=c++98

RM = rm -f

all: $(NAME)

$(NAME): $(OBJS)
	$(CXX) $(OBJS) -o $(NAME)

.cpp.o:		
	$(CXX) $(CXX_FLAGS) -c $< -o $(<:.cpp=.o) -MD

include $(wildcard $(D_FILE))

clean:
	$(RM) $(OBJS) $(D_FILE)

fclean: clean
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re

