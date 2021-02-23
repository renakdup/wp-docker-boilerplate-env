# Docker Boilerplate Environment for WordPress

Author: renakdup@gmail.com  
Github: https://github.com/renakdup  

## Instructions
1. You need to add the string to `hosts` file your OS:  
`127.0.0.1 	wp-docker-boilerplate.local`
2. Run command `Make d.up`
3. Visit site [wp-docker-boilerplate.local](http://wp-docker-boilerplate.local)

If you have a problems with access right for files, try using the next command for fixing it:  
`sudo chown USER:GROUP FILE`

If you want change domain, you need to change `server_name` in `./docker/nginxconf.d/default.conf`.


##  If you have troubles with VPN
1. If you use VPN, you need to disable VPN and run command:  
`docker network create localdev`
2. After It you can run your VPN.
3. Add the code at end of the file:
   ```networks:
    default:
     external:
      name: localdev
3. Make to  
 `docker-compose up -d`
 
 

