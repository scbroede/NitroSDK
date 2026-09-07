subdir('src')

libspi_includes = include_directories('include')

libspi = library('spi',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libspi_includes],
    pic: false,
    sources: [libspi_srcs, fx_const_h]
)

libspi_arm7 = library('spi_arm7',
    c_pch: nitro_pch,
    include_directories: [nitrosdk_includes, libspi_includes],
    pic: false,
    sources: [libspi_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

libtp_arm7 = library('tp_arm7',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libtp_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

libpm_arm7 = library('pm_arm7',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libpm_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

libmic_arm7 = library('mic_arm7',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libmic_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

libnvram_arm7 = library('nvram_arm7',
    c_pch: nitro_pch,
    include_directories: nitrosdk_includes,
    pic: false,
    sources: [libnvram_arm7_srcs, fx_const_h],
    dependencies: [nitrosdk_arm7_args_dep],
    c_args: ['-wrap:sdk', '2.0/sp2p3', '-USP1P3_BUG_FOR_CONDITIONAL_ASM_INSTRUCTIONS']
)

nitrosdk_libs += libspi
nitrosdk_arm7_libs += libspi_arm7
nitrosdk_arm7_libs += libtp_arm7
nitrosdk_arm7_libs += libpm_arm7
nitrosdk_arm7_libs += libmic_arm7
nitrosdk_arm7_libs += libnvram_arm7
