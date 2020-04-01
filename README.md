# Vue + Laravel 7
Starter template Vue + Laravel 7

## Getting Started
Follow all the steps in order to start the project

### Installing
Install composer dependecies

```
composer install
```

Install npm packages

```
npm i
```

Config your database in 
 ```
.env
 ```

Run migrations
 ```
php artisan migrate
 ```

Generate passport keys
 ```
php artisan passport:install
 ```

Add to .env your passport keys
 ```
PASSPORT_LOGIN_ENDPOINT=http://domain.com/oauth/token
PASSPORT_CLIENT_ID=2
PASSPORT_CLIENT_SECRET=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
 ```

You can see all you routes executing
 ```
php artisan route:list
 ```

### Generate User

Run tinker
 ```
php artisan tinker
 ```

Execute factory
 ```
factory('App\User')->create()
 ```

You result should be something like this
 ```
=> App\User {#3052
      name: "Ohara Jared",
      email: "ohara.jared@example.net",
      email_verified_at: "2019-10-07 19:18:24",
      updated_at: "2019-10-07 19:18:24",
      created_at: "2019-10-07 19:18:24",
      id: 1,
    }
 ```

### Test
We will use Postman to make the test, we will make a POST request to http://domain.com/api/login just sending the username and password fields of the user we want to authenticate.
In body we select form-data and add 

 ```
username: ohara.jared@example.net
password: password
 ```

Should return something like this

{"token_type":"Bearer","expires_in":31536000,"access_token":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}





