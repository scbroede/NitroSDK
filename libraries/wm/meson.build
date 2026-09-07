subdir('src')

libwm_includes = include_directories('include')

libwm = library('wm',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libwm_includes],
    pic: false,
    sources: [libwm_srcs, fx_const_h]
)

libwm_arm7_includes = include_directories('include/ARM7')

libwm_arm7 = library('wm_arm7',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libwm_includes, libwm_arm7_includes],
    pic: false,
    sources: [libwm_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

nitrosdk_arm7_libs += libwm_arm7

nitrosdk_libs += libwm
