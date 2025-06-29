termuxdc = cc.find_library('termux-display-client', dirs: [meson.project_source_root() + '/deps'])

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
