require 'dotenv'
Dotenv.load

# Load DSL and Setup Up Stages
require 'capistrano/setup'

# Includes default deployment tasks
require 'capistrano/deploy'

# Load tasks from gems
require 'capistrano/composer'

# Use wpcli to sync uploads and database
require 'capistrano/wpcli'

# Deploy theme submodule 
require "capistrano/scm/git"
install_plugin Capistrano::SCM::Git

require "capistrano/scm/git-with-submodules"
install_plugin Capistrano::SCM::Git::WithSubmodules

# Loads custom tasks from `lib/capistrano/tasks' if you have any defined.
# Customize this path to change the location of your custom tasks.
Dir.glob('lib/capistrano/tasks/*.cap').each { |r| import r }
