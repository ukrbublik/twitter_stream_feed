Simple web app to show last 25 tweets from you feed in real-time.

### Usage
- `composer install`
- Edit config.php
- Run socket server from command line: `php bin/ratchet.php`

### Heroku
- Buildpacks: `heroku/php` and `heroku/nodejs` (just for bower)
- Addons: `MemCachier`
- Separate Ratchet socket server to 2nd app. 
- Apps must have different `Procfile` files - 1st with contents of `Procfile1`, 2nd - of `Procfile2`
- Both apps must have same `MEMCACHIER_*` env vars and `IS_HEROKU=1`

### Demo
https://stream-feed.herokuapp.com/

