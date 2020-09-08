CC = tcc
EXT = .exe
CFLAGS = -Wall -std=c99
INCLUDE_PATHS_ = -I. -I$(RAYLIB_PATH)/src -I$(RAYLIB_PATH)/src/external
LDFLAGS = -Wl,-subsystem=console
LDLIBS = -lmsvcrt -lopengl32 -lgdi32 -lkernel32 -lshell32 -luser32 -lwinmm
PLATFORM = PLATFORM_DESKTOP

ALLSRC = \
	simple \
	bounce \
	sum

SRC = sum

all: $(SRC)

%: %.c
	$(CC) -o $@$(EXT) $< $(CFLAGS) $(INCLUDE_PATHS) $(LDFLAGS) $(LDLIBS) -D$(PLATFORM)

clean:
	@echo $(PLATFORM)
	del *.o *.exe /s
	@echo Cleaning done
