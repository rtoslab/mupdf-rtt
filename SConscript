from building import *

# get current directory
cwd     = GetCurrentDir()

# The set of source files associated with this SConscript file.
src     = Glob('cbz/*.c')
src    += Glob('draw/*.c')
src    += Glob('fitz/*.c')
src    += Glob('pdf/*.c')
src    += Glob('xps/*.c')

path    = [cwd + '/']
path   += [cwd + '/fitz']
path   += [cwd + '/pdf']
path   += [cwd + '/generated']

path   += [cwd + '/thirdparty/freetype/include']
path   += [cwd + '/thirdparty/zlib']

path   += [cwd + '/port']

group = DefineGroup('mupdf', src, depend = ['PKG_USING_MUPDF'], CPPPATH = path)

Return('group')
