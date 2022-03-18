project(CLPipeline.Core LANGUAGES C CXX)

find_package(OpenCL REQUIRED)

	add_library(${PROJECT_NAME})

	target_sources(${PROJECT_NAME} src)
	target_include_directories(${PROJECT_NAME} include)
	target_link_libraries(${PROJECT_NAME} OpenCL::OpenCL)

	set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 11)