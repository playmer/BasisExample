add_library(imgui "")

target_sources(imgui
    PRIVATE
        repo/imgui_demo.cpp
        repo/imgui_draw.cpp
        repo/imgui_internal.cpp
        repo/imgui_widgets.cpp
        repo/imgui.cpp
        repo/imgui.h
        repo/imstb_rectpack.h
        repo/imstb_textedit.h
        repo/imstb_truetype.h
        repo/examples/imgui_imp_sdl.cpp
        repo/examples/imgui_imp_sdl.h
)

target_include_directories(imgui
    PUBLIC
        repo
        repo/examples
)