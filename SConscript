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

src    += Split('''
    thirdparty/jpeg/jaricom.c \
    thirdparty/jpeg/jcomapi.c \
    thirdparty/jpeg/jdapimin.c \
    thirdparty/jpeg/jdapistd.c \
    thirdparty/jpeg/jdarith.c \
    thirdparty/jpeg/jdatadst.c \
    thirdparty/jpeg/jdatasrc.c \
    thirdparty/jpeg/jdcoefct.c \
    thirdparty/jpeg/jdcolor.c \
    thirdparty/jpeg/jddctmgr.c \
    thirdparty/jpeg/jdhuff.c \
    thirdparty/jpeg/jdinput.c \
    thirdparty/jpeg/jdmainct.c \
    thirdparty/jpeg/jdmarker.c \
    thirdparty/jpeg/jdmaster.c \
    thirdparty/jpeg/jdmerge.c \
    thirdparty/jpeg/jdpostct.c \
    thirdparty/jpeg/jdsample.c \
    thirdparty/jpeg/jdtrans.c \
    thirdparty/jpeg/jerror.c \
    thirdparty/jpeg/jfdctflt.c \
    thirdparty/jpeg/jfdctfst.c \
    thirdparty/jpeg/jfdctint.c \
    thirdparty/jpeg/jidctflt.c \
    thirdparty/jpeg/jidctfst.c \
    thirdparty/jpeg/jidctint.c \
    thirdparty/jpeg/jmemmgr.c \
    thirdparty/jpeg/jmemnobs.c \
    thirdparty/jpeg/jquant1.c \
    thirdparty/jpeg/jquant2.c \
    thirdparty/jpeg/jutils.c \
''')

src    += Split('''
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/bio.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/cio.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/dwt.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/event.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/image.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/j2k.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/j2k_lib.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/jp2.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/jpt.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/mct.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/mqc.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/openjpeg.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/pi.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/raw.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/t1.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/t2.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/tcd.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/tgt.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/cidx_manager.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/phix_manager.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/ppix_manager.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/thix_manager.c \
    thirdparty/openjpeg-1.5.0-patched/libopenjpeg/tpix_manager.c \
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
