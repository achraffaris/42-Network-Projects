NAME = so_long.a
NAME_BONUS = so_long_bonus.a

CC = cc
CFLAGS = -Wall -Wextra -Werror 
AR = ar rc
MLX = -L /usr/local/lib -lmlx -framework OpenGl -framework Appkit 

SRCS = 	so_long.c \
		utils/gnl/get_next_line_utils.c \
		utils/gnl/get_next_line.c \
		utils/map/map_checker.c \
		utils/map/images_renderer.c \
		utils/map/map.c \
		utils/map/map_checker.c \
		utils/str/str_utils.c \
		utils/utils.c \
		utils/str/itoa.c \
		utils/str/strjoin.c \
		utils/events/movements.c \
		utils/events/events_manager.c \
		
BSRCS = so_long_bonus.c \
		bonus/bonus_utils/gnl/get_next_line_utils.c \
		bonus/bonus_utils/gnl/get_next_line.c \
		bonus/bonus_utils/map/map_checker.c \
		bonus/bonus_utils/map/images_renderer.c \
		bonus/bonus_utils/map/map.c \
		bonus/bonus_utils/map/map_checker.c \
		bonus/bonus_utils/str/str_utils.c \
		bonus/bonus_utils/utils.c \
		bonus/bonus_utils/str/itoa.c \
		bonus/bonus_utils/str/strjoin.c \
		bonus/bonus_utils/events/movements.c \
		bonus/bonus_utils/events/events_manager.c \
		bonus/bonus_utils/events/animation.c \
		bonus/bonus_utils/events/utils.c \
		bonus/bonus_utils/map/images_init.c
		
BOBJS = $(BSRCS:.c=.o)
OBJS = $(SRCS:.c=.o)

all: $(NAME)

$(NAME): $(OBJS)
	@rm -rf $(NAME_BONUS)
	@$(AR) $(NAME) $(OBJS)
	@$(CC) $(CFLAGS) $(NAME) $(MLX) -o so_long

bonus: $(NAME_BONUS)

$(NAME_BONUS): $(BOBJS)
	@rm -rf $(NAME)
	@$(AR) $(NAME_BONUS) $(BOBJS)
	@$(CC) $(CFLAGS) $(NAME_BONUS) $(MLX) -o so_long 

clean:
	@rm -rf $(OBJS) $(BOBJS)

fclean: clean
	@rm -rf $(NAME) $(NAME_BONUS)
	@rm -rf so_long

re : fclean all

.PHONY: re fclean all clean bonus