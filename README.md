
# tunnel_monitor

## CRON

````toml
# Cron Triggers
# Docs: https://developers.cloudflare.com/workers/platform/triggers/cron-triggers/
# Configuration: https://developers.cloudflare.com/workers/wrangler/configuration/#triggers
[triggers]
crons = ["* * * * *"] # * * * * * = run every minute
````

````javascript

  "scripts": {
    "deploy": "wrangler deploy",
    "dev": "wrangler dev",
    "start": "wrangler dev",
    "start-job": "wrangler dev --test-scheduled"
  }
````

````bash

curl "http://localhost:8787/__scheduled?cron=*+*+*+*+*"

````

## D1

````toml
[[ d1_databases ]]
binding = "DB" # available in your Worker on `env.DB`
database_name = "d1"
database_id = "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"


````

````bash



npm install wrangler --g

wrangler d1 execute d1 --command "SELECT name FROM sqlite_schema WHERE type ='table'"
````

````bash

echo "# tunnel_monitor" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/joaosgomes/tunnel_monitor.git
git push -u origin main
````