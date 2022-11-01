# Rake Tasks
# desc 'outputs hello to the terminal'
# task :hello do
#   puts "hello from Rake!"
# end

# desc 'outputs hola to the terminal'
# task :hola do
#   puts "hola de Rake!"
# end

# Namespacing Rake Tasks
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

# Common Rake Tasks
# environment task to load Student class and database connection first
task :environment do
    require_relative './config/environment'
  end
# migrate, seed rake task
namespace :db do
  #migrate task
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  #seed task
  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

#Rake console task - interact with db and class
desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

