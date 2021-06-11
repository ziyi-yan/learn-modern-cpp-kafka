find_package(PkgConfig REQUIRED) 

if(APPLE)
    # For pkg-config to find openssl@1.1 from Homebrew
    set(ENV{PKG_CONFIG_PATH} "$ENV{PKG_CONFIG_PATH}:/usr/local/opt/openssl@1.1/lib/pkgconfig")
endif()
pkg_check_modules(RDKAFKA REQUIRED IMPORTED_TARGET rdkafka)

add_executable(main main.cc)

target_link_libraries(main PUBLIC PkgConfig::RDKAFKA)
