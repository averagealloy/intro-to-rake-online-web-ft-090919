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
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
    end
    desc 'seed the database with some dummy data'
    task :seed do
      require_relative './db/seeds.rb'
      desc 'giving access to the to the config enviroment'
      task :environment do
        require_relative './config/environment'
      end
    end
end

desc 'drop into the pry console'
task :console => :enviroment do
  Pry.start
end
