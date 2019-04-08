ifeq ($(SHLIB_EXT), dll)
	libdir=$(prefix)/bin
else
	libdir=$(prefix)/lib
endif

install:
	$(CC) $(CPPFLAGS) $(CFLAGS) $(LDFLAGS) -O2 -shared -fPIC -I $(prefix)/include extractors.c -o $(libdir)/libtestu01extractors.$(SHLIB_EXT) -L $(prefix)/lib $(RPATH) -lmylib -lprobdist -ltestu01

# Makefile debugging trick:
# call print-VARIABLE to see the runtime value of any variable
print-%:
	@echo '$*=$($*)'
