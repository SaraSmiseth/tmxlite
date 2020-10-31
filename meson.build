project('tmxlite', 'cpp')

tmxlite_includes = include_directories('tmxlite/include')

miniz_project = subproject('miniz')
miniz_dependency = miniz_project.get_variable('miniz_dependency')

pugixml_project = subproject('pugixml')
pugixml_dependency = pugixml_project.get_variable('pugixml_dependency')

tmxlite_sources = [
'tmxlite/src/FreeFuncs.cpp',
'tmxlite/src/ImageLayer.cpp',
'tmxlite/src/LayerGroup.cpp',
'tmxlite/src/Map.cpp',
'tmxlite/src/Object.cpp',
'tmxlite/src/ObjectGroup.cpp',
'tmxlite/src/Property.cpp',
'tmxlite/src/TileLayer.cpp',
'tmxlite/src/Tileset.cpp',
]

tmxlite_library = library('tmxlite', sources : tmxlite_sources, include_directories : tmxlite_includes, dependencies: [miniz_dependency, pugixml_dependency])

tmxlite_dependency = declare_dependency(include_directories : tmxlite_includes, link_with : tmxlite_library)
