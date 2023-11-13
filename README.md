# Medusa-Ecommerce-Demo
Demo ecommerce platform using Medusa. 

Based on : https://www.freecodecamp.org/news/how-to-build-your-own-e-commerce-site-with-medusa/

https://lo-victoria.com/how-to-build-a-nextjs-e-commerce-website-with-medusa

### Set-up
Ensure that postgresql is installed

Gitpod provides several images that enable us to use databases. 
https://www.gitpod.io/guides/gitpodify#postgresql

To use PostgreSQL database, create a `.gitpod.yml` file and add the following line:
```YML
image: gitpod/workspace-postgres
```

This will give us an auto-starting PostgreSQL server. We need push and commit the YML file to github, then open up a new workspace. Restarting the existing workspace will not work. 

We can use `psql -h localhost -d postgres` to interact with postgres, create other users etc. 

First we install the medusa cli
```
npm install @medusajs/medusa-cli -g
```

Create a new medusa app
```
npx create-medusa-app@latest
```

Note that the default user and password for postgres is gitpod.

Postgres Troubleshooting tips: https://stackoverflow.com/questions/15301826/psql-fatal-role-postgres-does-not-exist

We also have the option to configure the Postgresql DB with Supabase or Vercel Postgresql


### Running the App
- To run the app backend, cd to `my-medusa-store` and run `npx medusa develop` or `npm run dev`
- To run the storefront, cd to `my-medusa-store-storefront` and run `npm run dev`

The following ports will be running:
- 5432 Default Postgresql port (Should always be running)
- 9000 App Backend and API
- 7001 Admin Dashboard
- 8000 Storefront

The default admin credentials
```
email: admin@medusa-test.com
password: superuser
```

Note: I am unable to access the admin page when running on gitpod. This is a known problem:
https://github.com/medusajs/medusa/discussions/4822