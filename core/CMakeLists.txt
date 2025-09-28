find_package(Qt6 COMPONENTS Widgets REQUIRED)

qt_add_executable(SDGDCheat
        Core.Main.cpp
)
add_custom_command(TARGET SDGDCheat POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different
        C:/Qt/6.9.1/mingw_64/bin/Qt6Widgets.dll
        $<TARGET_FILE_DIR:SDGDCheat>
        COMMAND ${CMAKE_COMMAND} -E copy_if_different
        C:/Qt/6.9.1/mingw_64/bin/Qt6Gui.dll
        $<TARGET_FILE_DIR:SDGDCheat>
        COMMAND ${CMAKE_COMMAND} -E copy_if_different
        C:/Qt/6.9.1/mingw_64/bin/Qt6Core.dll
        $<TARGET_FILE_DIR:SDGDCheat>
)


target_link_libraries(SDGDCheat PRIVATE Qt6::Widgets)

