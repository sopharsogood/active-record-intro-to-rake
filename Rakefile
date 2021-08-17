namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
     puts "hello from Rake!"
  end
  desc 'outputs hola to the terminal'
  task :hola do
     puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrates changes to database'
  task :migrate => :environment do
     Student.create_table
  end

  desc 'seed the database with dummy data for testing'
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end
end

desc 'requires environment file'
task :environment do
  require_relative './config/environment.rb'
end

desc 'drop into Pry console'
task :console do
  Pry.start
end