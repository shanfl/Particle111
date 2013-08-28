project(PSApi)
set(PSApi 
	system.cpp
	action_api.cpp
	actions.cpp
	opengl.cpp
	p_vector.h
	papi.h
)
add_library(particle STATIC ${PSApi})

set(PSpray_src PSpray.cpp)
add_executable(PSpray ${PSpray_src})
target_link_libraries(PSpray particle)