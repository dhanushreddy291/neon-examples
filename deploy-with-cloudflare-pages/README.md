<img width="250px" src="https://neon.tech/brand/neon-logo-dark-color.svg" />

# Getting started with Neon and Cloudflare Pages

This is the code repository for the guide on how to [deploy a Cloudflare Pages web application using Neon](https://neon.tech/docs/guides/cloudflare-pages). Follow the guide to set up the Neon project and your Cloudflare Pages application.

## Store your Neon credentials

Run the command below to copy the `.env.example` file:

```
cp .env.example .env
```

Store your Neon credentials in this `.env` file.

```
DATABASE_URL="postgresql://neondb_owner:...@ep-...us-east-1.aws.neon.tech/neondb?sslmode=require"
```

- `user` is the database user.
- `password` is the database user’s password.
- `endpoint_hostname` is the host with neon.tech as the [TLD](https://www.cloudflare.com/en-gb/learning/dns/top-level-domain/).
- `dbname` is the name of the database. “neondb” is the default database created with each Neon project.
- `?sslmode=require` an optional query parameter that enforces the [SSL](https://www.cloudflare.com/en-gb/learning/ssl/what-is-ssl/) mode while connecting to the Postgres instance for better security.

**Important**: To ensure the security of your data, never expose your Neon credentials to the browser.

## Test the application locally

Run the command below to deploy the application locally:

```bash
npx wrangler pages dev -- npm run dev
```

## Deploy the application to Cloudflare Pages

Follow the guide for instructions on how to deploy the application to the Cloudflare platform. Make sure to add the Neon credentials to the Cloudflare Pages environment variables.