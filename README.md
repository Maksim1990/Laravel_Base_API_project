
**HOT TO INSTALL APP**
--
     
* *Start app and build required Docker containers:*

        docker-compose up -d
      
* *Install all composer dependencies:*

        docker exec -it laravel_api composer install
        
* *Copy ``.env`` environment config file and set all required settings in it:*

        docker exec -it laravel_api cp .env.dist .env

* *Generate Laravel application key:*

        docker exec -it laravel_api php artisan key:generate
        
* *Run all required migrations:*

        docker exec -it laravel_api php artisan migrate
  
* *Generate the encryption keys needed to generate secure access Passport JWT tokens:*
    
        docker exec -it laravel_api  php artisan passport:install

App is available on ``8187`` port
--
    http://127.0.0.1:8187

**Mail Server**
--
*Mail development server is available on ``8127`` port*
        
    http://127.0.0.1:8127