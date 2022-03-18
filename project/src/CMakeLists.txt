add_library(src 
            test.h
            test.cpp

            # imgui_impl_sdl.cpp
            # imgui_impl_sdl.h
            # imgui_impl_sdlrenderer.cpp
            # imgui_impl_sdlrenderer.h

            # imgui.cpp
            # imgui.h
            # imgui_demo.cpp
            # imgui_draw.cpp
            # imgui_internal.h
            # imconfig.h
            # imstb_rectpack.h
            # imstb_textedit.h
            # imstb_truetype.h
            )

target_include_directories(src PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}" SDL2 SDL2main SDL2_ttf imgui)