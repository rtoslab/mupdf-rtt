from building import *

cwd     = GetCurrentDir()
src     = Glob('cbz/*.c')
CPPPATH = [cwd]

group = DefineGroup('mupdf', src, depend = ['PKG_USING_MUPDF'], CPPPATH = CPPPATH)

Return('group')
