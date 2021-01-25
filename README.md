#Guidelines for laravel project

1. cd x-backend
2. cp .env.example .env
 - nano .env
 - DB_HOST=db
 - DB_DATABASE=sanctumauth
 - DB_USERNAME=sanctumauth_user
 - DB_PASSWORD=password

3. docker-compose build app
4. docker-compose up -d

# Not needed
5. docker-compose ps
6. docker-compose exec app ls -l

# Needed
7. docker-compose exec app composer install (Installing Composer)
8. docker-compose exec app php artisan key:generate (Generate Application key in .env file)
9. docker-compose exec app php artisan migrate:fresh --seed (Migrate database and seeders)
# http://127.0.0.1:8000/

10. shut down compose file and remove container -> docker-compose down