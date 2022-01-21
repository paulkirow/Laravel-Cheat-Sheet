# Laravel Cheat Sheet
A collection of commands I've found useful while working in Laravel :shipit:

### Laravel

| Command | Description |
| --- | --- |
| `php artisan make:model Photo -m -f -c -r -s --policy` | Generate a model, migration, factory, controller, resource, seeder, and policy |
| `php artisan generate:factory` | Generates factories based on the db schema's for all models which don't have them already |

| `php artisan make:middleware HandleSomething` | Create a middleware in the project |
| `php artisan make:test PurchaseTicketsTest` | Create a test in the Feature directory |
| `php artisan make:test UserTest --unit` | Create a test in the Unit directory |
| `php artisan db:seed --class=SeederFile` | Run a seeder |
| `php artisan tinker --database=dbname` | Run tinker against a specifc database |
| `php artisan migrate:fresh --seed` | Drop the schema and recreate it then run the seeders |


### Laravel Sail [:blue_book:](https://laravel.com/docs/8.x/sail)
Local Laravel environment in docker.
| Command | Description |
| --- | --- |
| `alias sail='bash vendor/bin/sail'` | Alias sail so it can subsaquently be called with just `sail` |
| `sail up -d` | Create and start containers, detached to run without taking over your console |
| `sail down` | Stop and remove resources |
| `sail artisan ...` | Run artisan commands inside the container |

### Laravel Breeze [:blue_book:](https://laravel.com/docs/8.x/starter-kits#laravel-breeze)

Minimal implementation of authentication in Laravel.

| Command | Description |
| --- | --- |
| `composer require laravel/breeze --dev` | Add Breeze to the project |
| `php artisan breeze:install` | Publish Breeze files to the project |

### Laravel Scout + Algolia [:blue_book:](https://laravel.com/docs/8.x/scout) [:blue_book:](https://www.algolia.com/doc/framework-integration/laravel/getting-started/introduction-to-scout-extended/?client=php)

| Command | Description |
| --- | --- |
| `php artisan scout:sync "Postings"` | Update the configuration of a Model's index |
| `php artisan scout:import "Postings"` | Empty the index and import all the records from the Model |
| `php artisan scout:reimport "Postings"` | (Algolia) Import the Model records and swap them with the current records in the index |
| `php artisan scout:optimize "Postings"` | (Algolia) Optimize the given searchable creating a settings file |
| `php artisan scout:make-aggregator Postings` | (Algolia) Creates an "aggregator", a combination of multiple Models into a single index |

### Git [:blue_book:](https://cli.github.com/)

| Command | Description |
| --- | --- |
| `git symbolic-ref refs/heads/shortcut refs/heads/originbranch` | Create a local alternative name for a branch |
| `gh alias set pcw 'create --web'` | Using GitHub CLI create an alias to open the "create merge request" page to main |
| `gh alias set pcwd 'create --web --base branch_name'` | Using GitHub CLI create an alias to open the "create merge request" page to a specific branch |
| `php artisan make:test UserTest --unit` | Create a test in the Unit directory |


### Misc

| Command | Description |
| --- | --- |
| `svgo "icon.svg"` | Optimize a svg icon |
| `phpunit tests.php --filter=testMethod --repeat 1000` | Run a specific test repeating 1000 times |
| `mysqldump -uuser -ppassword --single-transaction --order-by-primary --result-file db-backup-``date +%F``.sql databasename` | Create a dump of a database |
| `php artisan make:test UserTest --unit` | Create a test in the Unit directory |
| `composer dump-autoload` | Composer: If you need to update the autoloader because of new classes in a classmap package |
| `composer outdated` | Check outdated composer packages |
| `composer upgrade --lock` | Regenerate composer.lock based on composer.json |
| `php artisan backpack:crud <model-name>` | Backpack for Laravel: Create a CRUD (Creates CRUD Controller, Model, Request, Migration) |
| `php artisan backpack:publish crud/fields/<field name>` | Backpack for Laravel: Creates a copy of a particular field in the project files so it can be customized |



