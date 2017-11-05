# Homestead-Salty
Simple way to comunicate with vagrant Homestead.

##Motivation

After a while using vagrant ssh to enter to the homestead box and execute simple commands like 'art make controller' and such, i start noticing the waste of time doing vagrant ssh, after see the shipping-docker/vessel package where you can do the commands on you project directory and that will reflect on the server. I built a small script to do the same with laravel homestead.

##Examples

```
./salty art route:list
```
In this example we are doing the same as:
```
cd Homestead
vagrant ssh
cd /Code/[project_folder]
art route:list
```

## Configurations
Thats not much to talk here, the only configurations that are used in this script is the .env file so if it is configured properlly everiting will work fine.

## What's avalable ?
| Command       | Similar       |
| ------------- |:-------------:|
| ./salty artisan [args]     | same thing as 'php artisan' on homestead machine |
| ./salty art [args]      | short form to './salty artisan [args]'      |
| ./salty composer [args] | same thing as 'composer [args]' on homestead machine      |
| ./salty comp [args] | short form to './salty composer [args]'      |
| ./salty phpunit |  same thing as 'phpunit' on homestead machine      |
| ./salty p [args] | short form to './salty phpunit [args]'     |
| ./salty filter [args] |  same thing as 'phpunit --filter [args]' on homestead machine      |
| ./salty pf [args] | short form to './salty phpunit --filter [args]'     |
| ./salty seed |  same thing as 'php artisan db:seed' on homestead machine      |
| ./salty dump |  creates a dump of the database specified on .env file as DB_DATABASE      |
| ./salty create:db |  creates a database based on DB_DATABASE specified on .env file      |

# Happy Hacking


