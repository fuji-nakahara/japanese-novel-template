require 'yaml'

desc 'Create git tag and push it'
task :tag do
  config_path = File.expand_path('_config.yml', __dir__)
  config      = YAML.load_file(config_path)
  version     = config['version']

  system "git tag -m 'Version #{version}' v#{version}"
  system 'git push'
  system 'git push --tags'
end
