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
    thirdparty/freetype/src/base/ftbase.c \
    thirdparty/freetype/src/base/ftbbox.c \
    thirdparty/freetype/src/base/ftbitmap.c \
    thirdparty/freetype/src/base/ftgasp.c \
    thirdparty/freetype/src/base/ftglyph.c \
    thirdparty/freetype/src/base/ftinit.c \
    thirdparty/freetype/src/base/ftstroke.c \
    thirdparty/freetype/src/base/ftsynth.c \
    thirdparty/freetype/src/base/ftsystem.c \
    thirdparty/freetype/src/base/fttype1.c \
    thirdparty/freetype/src/base/ftxf86.c \
    thirdparty/freetype/src/autofit/autofit.c \
    thirdparty/freetype/src/bdf/bdf.c \
    thirdparty/freetype/src/cff/cff.c \
    thirdparty/freetype/src/cid/type1cid.c \
    thirdparty/freetype/src/gzip/ftgzip.c \
    thirdparty/freetype/src/lzw/ftlzw.c \
    thirdparty/freetype/src/pcf/pcf.c \
    thirdparty/freetype/src/pfr/pfr.c \
    thirdparty/freetype/src/psaux/psaux.c \
    thirdparty/freetype/src/pshinter/pshinter.c \
    thirdparty/freetype/src/psnames/psnames.c \
    thirdparty/freetype/src/raster/raster.c \
    thirdparty/freetype/src/sfnt/sfnt.c \
    thirdparty/freetype/src/smooth/smooth.c \
    thirdparty/freetype/src/truetype/truetype.c \
    thirdparty/freetype/src/type1/type1.c \
    thirdparty/freetype/src/type42/type42.c \
    thirdparty/freetype/src/winfonts/winfnt.c \
''')

src    += Split('''
    thirdparty/jbig2dec/jbig2_arith.c \
    thirdparty/jbig2dec/jbig2_arith_int.c \
    thirdparty/jbig2dec/jbig2_arith_iaid.c \
    thirdparty/jbig2dec/jbig2_huffman.c \
    thirdparty/jbig2dec/jbig2_segment.c \
    thirdparty/jbig2dec/jbig2_page.c \
    thirdparty/jbig2dec/jbig2_symbol_dict.c \
    thirdparty/jbig2dec/jbig2_text.c \
    thirdparty/jbig2dec/jbig2_halftone.c \
    thirdparty/jbig2dec/jbig2_generic.c \
    thirdparty/jbig2dec/jbig2_refinement.c \
    thirdparty/jbig2dec/jbig2_mmr.c \
    thirdparty/jbig2dec/jbig2_image.c \
    thirdparty/jbig2dec/jbig2_metadata.c \
    thirdparty/jbig2dec/jbig2.c \
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

CPPDEFINES  = ['FT2_BUILD_LIBRARY', 'HAVE_STDINT_H']

group = DefineGroup('mupdf', src, depend = ['PKG_USING_MUPDF'], CPPDEFINES = CPPDEFINES, CPPPATH = path)

Return('group')
