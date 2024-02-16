from building import *
import rtconfig

# get current directory
cwd     = GetCurrentDir()
# The set of source files associated with this SConscript file.
src     = []
#src += Glob(cwd+"/common/src/*.c")
if GetDepend(['PKG_USING_LEVEL_NOR']):
    src += Glob(cwd+"/common/src/lx_nor*.c")
if GetDepend(['PKG_USING_LEVEL_NAND']):
    src += Glob(cwd+"/common/src/lx_nand*.c")


path    = [cwd + '/common/inc']
path += [cwd + '/ports/generic/inc']
group = DefineGroup('Levelx', src, depend = ['PKG_USING_LEVELX'], CPPPATH = path)

Return('group')
