set_source_group(SOURCES "Source Files" createirepformfrombinary.cc
    createirepfrombinary.cc
    dwarfgen.cc irepattrtodbg.cc ireptodbg.cc
    ../../lib/libdwarf/dwgetopt.c)
    
set_source_group(HEADERS "Header Files" createirepfrombinary.h
    general.h irepattrtodbg.h 
    irepdie.h irepform.h irepframe.h 
    irepline.h irepmacro.h ireppubnames.h 
    irepresentation.h ireptodbg.h strtabdata.h
    ../../lib/libdwarf/dwgetopt.h)

set_source_group(CONFIGURATION_FILES "Configuration Files" 
    ${CMAKE_SOURCE_DIR}/cmake/config.h.cmake
    ${CMAKE_BINARY_DIR}/config.h)
    
add_executable(dwarfgen ${SOURCES} ${HEADERS} ${CONFIGURATION_FILES})

set_folder(dwarfgen src/bin/dwarfgen)

target_compile_options(dwarfgen PRIVATE ${DW_FWALLXX})

target_link_libraries(dwarfgen PRIVATE ${dwarf-target} ${DW_FZLIB})

set(SUFFIX $<$<EQUAL:${CMAKE_SIZEOF_VOID_P},8>:64>)
set(LIBDIR lib${SUFFIX})
set(BINDIR bin${SUFFIX})

install(TARGETS dwarfgen DESTINATION
	RUNTIME DESTINATION ${BINDIR}		
	LIBRARY DESTINATION ${LIBDIR}
	ARCHIVE DESTINATION ${LIBDIR})

#install(FILES dwarfgen.conf DESTINATION lib)

#install(FILES dwarfgen.1 DESTINATION share/man/man1)
