subdir('src')

libcard_includes = include_directories('include')

libcard = library('card',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libcard_includes],
    pic: false,
    sources: [libcard_srcs, fx_const_h],
)

libcard_arm7 = library('card_arm7',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libcard_includes],
    pic: false,
    sources: [libcard_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

nitrosdk_libs += libcard
nitrosdk_arm7_libs += libcard_arm7
