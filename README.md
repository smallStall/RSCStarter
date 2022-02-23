# Summary
This is a Starter with Supabase, Remix, and Cloudflare Workers.

# Use
```bash
git clone https://github.com/smallStall/RSCStarter
cd RSCStarter
npm install
```
Let's create the Cloudflare Workers configuration file wrangler.toml as follows.
```toml:wrangler.toml
name = "remix-supabase-cloudflare-workers-starter"
type = "javascript"

zone_id = ""
account_id = ""
route = ""
workers_dev = true

[site]
bucket = "./public"
entry-point = "."

[build]
command = "npm run build:worker"
watch_dir = "build/index.js"

[build.upload]
format="service-worker"
```
