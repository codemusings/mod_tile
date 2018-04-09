cc = meson.get_compiler('c')

sources = [
    'daemon.c',
    'gen_tile.cpp',
    'request_queue.c'
]

mapnik_dep = cc.find_library('mapnik')

executable('renderd',
    include_directories: [includes, iniparser_include],
    sources: sources,
    dependencies: [
        iniparser_dep,
        dependency('threads'),
        mapnik_dep
    ]
)
