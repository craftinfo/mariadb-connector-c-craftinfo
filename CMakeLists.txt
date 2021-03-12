cmake_minimum_required( VERSION 3.0)

project( mariadb-connector-c-craftinfo NONE)

# install craftinfos

file( GLOB DEFINITION_DIRS
   definition*
)

if( DEFINITION_DIRS)
	foreach( DIR ${DEFINITION_DIRS} )
	   install( DIRECTORY "${DIR}" DESTINATION "share/mulle-craft/mariadb-connector-c"
	            USE_SOURCE_PERMISSIONS
	            PATTERN "*._DS_Store" EXCLUDE
	   )
	endforeach()
else()
   message( FATAL_ERROR "Remove craftinfo \"mariadb-connector-c\" as it is empty with:\n   mulle-sourcetree remove craftinfo/mariadb-connector-c\n   rm -rf craftinfo/mariadb-connector-c")
endif()
