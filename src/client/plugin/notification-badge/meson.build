
plugin_name = 'notification-badge'

plugin_src = files(
  plugin_name + '.vala',
  'unity-launcher-entry.vala'
)
plugin_data = join_paths(plugin_name + '.plugin')
plugin_dest = join_paths(plugins_dir, plugin_name)

shared_module(
  plugin_name,
  sources: plugin_src,
  dependencies: plugin_dependencies,
  include_directories: config_h_dir,
  vala_args: geary_vala_args,
  c_args: plugin_c_args,
  install: true,
  install_dir: plugin_dest
)

i18n.merge_file(
  input: plugin_data + '.in',
  output: plugin_data,
  type: 'desktop',
  po_dir: po_dir,
  install: true,
  install_dir: plugin_dest
)
