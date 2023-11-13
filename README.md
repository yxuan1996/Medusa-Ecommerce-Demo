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


First we install the medusa cli
```
npm install @medusajs/medusa-cli -g
```

Create a new medusa app
```
npx create-medusa-app@latest
```