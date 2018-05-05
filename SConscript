from building import *

# get current directory
cwd     = GetCurrentDir()

# The set of source files associated with this SConscript file.
src     = Glob('cbz/*.c')
src    += Glob('draw/*.c')
src    += Glob('fitz/*.c')
src    += Glob('pdf/*.c')
src    += Glob('xps/*.c')

src    += Split('''
    3rdparty/freetype/src/base/ftbase.c \
    3rdparty/freetype/src/base/ftbbox.c \
    3rdparty/freetype/src/base/ftbitmap.c \
    3rdparty/freetype/src/base/ftgasp.c \
    3rdparty/freetype/src/base/ftglyph.c \
    3rdparty/freetype/src/base/ftinit.c \
    3rdparty/freetype/src/base/ftstroke.c \
    3rdparty/freetype/src/base/ftsynth.c \
    3rdparty/freetype/src/base/ftsystem.c \
    3rdparty/freetype/src/base/fttype1.c \
    3rdparty/freetype/src/base/ftxf86.c \
    3rdparty/freetype/src/autofit/autofit.c \
    3rdparty/freetype/src/bdf/bdf.c \
    3rdparty/freetype/src/cff/cff.c \
    3rdparty/freetype/src/cid/type1cid.c \
    3rdparty/freetype/src/gzip/ftgzip.c \
    3rdparty/freetype/src/lzw/ftlzw.c \
    3rdparty/freetype/src/pcf/pcf.c \
    3rdparty/freetype/src/pfr/pfr.c \
    3rdparty/freetype/src/psaux/psaux.c \
    3rdparty/freetype/src/pshinter/pshinter.c \
    3rdparty/freetype/src/psnames/psnames.c \
    3rdparty/freetype/src/raster/raster.c \
    3rdparty/freetype/src/sfnt/sfnt.c \
    3rdparty/freetype/src/smooth/smooth.c \
    3rdparty/freetype/src/truetype/truetype.c \
    3rdparty/freetype/src/type1/type1.c \
    3rdparty/freetype/src/type42/type42.c \
    3rdparty/freetype/src/winfonts/winfnt.c \
''')

path    = [cwd + '/']
path   += [cwd + '/fitz']
path   += [cwd + '/pdf']
path   += [cwd + '/generated']

path   += [cwd + '/thirdparty/freetype/include']
path   += [cwd + '/thirdparty/jbig2dec']
path   += [cwd + '/thirdparty/jpeg']
path   += [cwd + '/thirdparty/openjpeg/libopenjpeg']
path   += [cwd + '/thirdparty/zlib']

path   += [cwd + '/port']

group = DefineGroup('mupdf', src, depend = ['PKG_USING_MUPDF'], CPPPATH = path)

Return('group')
