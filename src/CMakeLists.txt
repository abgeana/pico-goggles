add_executable(goggles
    main.cpp
)

target_link_libraries(goggles
    pico_stdlib
    hardware_pio
)

pico_generate_pio_header(goggles ${CMAKE_CURRENT_LIST_DIR}/ws2812.pio)

pico_enable_stdio_usb(goggles 1)
pico_enable_stdio_uart(goggles 0)

pico_add_extra_outputs(goggles)
