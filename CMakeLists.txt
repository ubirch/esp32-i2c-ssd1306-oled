set(COMPONENT_SRCS
        main/font_glcd_5x7.c
        main/font_tahoma_8pt.c
        main/fonts.c
        main/i2c.c
        main/ssd1306_i2c.c
        )
set(COMPONENT_ADD_INCLUDEDIRS "main/include")
register_component()