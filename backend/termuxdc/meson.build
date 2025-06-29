termuxdc = cc.find_library('termux-display-client', dirs: ['deps'])

if not termuxdc.found()
    error('termux-display-client not found in deps directory')
endif

if not termuxdc.found()
	subdir_done()
endif

wlr_files += files(
	'backend.c',
	'output.c',
	'input.c',
	'allocator.c',
)

wlr_deps += termuxdc
features += { 'termuxdc-backend': true }
