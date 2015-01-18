project(evpng)
set ( EV_LIBPNG_SRCS
png.c
png.h
pngconf.h
pngdebug.h
pngerror.c
pngget.c
pnginfo.h
pnglibconf.h
pngmem.c
pngpread.c
pngpriv.h
pngread.c
pngrio.c
pngrtran.c
pngrutil.c
pngset.c
pngstruct.h
pngtrans.c
pngwio.c
pngwrite.c
pngwtran.c
pngwutil.c
)

#add_library( evpng STATIC ${EV_LIBPNG_SRCS} )
#add_library( png ${EV_LIBPNG_SRCS} )
target_link_libraries( png z ) 

install(TARGETS png DESTINATION lib)
install(FILES png.h DESTINATION include)