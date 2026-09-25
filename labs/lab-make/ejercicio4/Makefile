# Nombre del ejecutable final
PROGRAMA := programa

# Compilador y flags
CC     := gcc
CFLAGS := -Wall

# Lista de archivos fuente .c
SRCS := main.c operaciones.c

# Archivos objeto generados a partir de SRCS
OBJS := $(SRCS:.c=.o)

# Regla principal
all: $(PROGRAMA)

# Linkear todos los objetos para generar el ejecutable final
$(PROGRAMA): $(OBJS)
	$(CC) $^ -o $(PROGRAMA)

# Compilar cualquier archivo .c en su .o correspondiente
%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Regla para limpiar archivos generados
clean:
	rm -f $(PROGRAMA) $(OBJS)

.PHONY: all clean
