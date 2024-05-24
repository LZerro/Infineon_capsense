from building import *
import rtconfig
Import('RTT_ROOT')

# get current directory
cwd = GetCurrentDir()
src = []
path = [cwd]

if GetDepend(['BSP_USING_SLIDER']):
    src += ['cy_capsense_control.c']
    src += ['cy_capsense_sensing.c']
    src += ['cy_capsense_sensing_v2.c']
    src += ['cy_capsense_csx_v2.c']
    src += ['cy_capsense_csd_v2.c']
    src += ['cy_capsense_processing.c']
    src += ['cy_capsense_tuner.c']
    src += ['cy_capsense_structure.c']
    src += ['cy_capsense_centroid.c']
    src += ['cy_capsense_filter.c']
    if rtconfig.PLATFORM in ['armclang']:
        src += ['lib/cy_capsense.lib']

group = DefineGroup('Libraries', src, depend=[''], CPPPATH=path)

Return('group')
