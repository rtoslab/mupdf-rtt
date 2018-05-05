from building import *

# get current directory
cwd     = GetCurrentDir()

# The set of source files associated with this SConscript file.
src     = Glob('cbz/*.c')

path    = [cwd + '/']
path   += [cwd + '/fitz']
path   += [cwd + '/port']

group = DefineGroup('mupdf', src, depend = ['PKG_USING_MUPDF'], CPPPATH = path)

Return('group')
