add_library(Mem.Core STATIC
        Mem.Core.Main.cpp
        Mem.Core.Main.h
)

target_link_libraries(Mem.Core PRIVATE
    Mem.Manipulator

)