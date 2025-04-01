# MVP TEMPLATE
A minimal Next.js starter template featuring Supabase, Prisma, Tailwind CSS, and Shadcn/UI, deployed with Vercel.

## Features

- Works across the entire [Next.js](https://nextjs.org) stack
  - App Router
  - Pages Router
  - Middleware
  - Client
  - Server
 
- supabase-ssr. A package to configure Supabase Auth to use cookies
- Prisma Integration
    - Easy database management with Prisma ORM

- Styling with [Tailwind CSS](https://tailwindcss.com)
- Components with [shadcn/ui](https://ui.shadcn.com/)
- Optional deployment with [Supabase Vercel Integration and Vercel deploy](#deploy-your-own)
  - Environment variables automatically assigned to Vercel project



## Deploy to Vercel
Vercel deployment will guide you through creating a Supabase account and project.

After installation of the Supabase integration, all relevant environment variables will be assigned to the project so the deployment is fully functioning.

The above will also clone the MVP-Template to your GitHub, you can clone that locally and develop locally.

If you wish to just develop locally and not deploy to Vercel, [follow the steps below](#Local-Development).

## Local Development
To develop locally without deploying to Vercel, follow these steps:

1. You'll first need a Supabase project which can be made [via the Supabase dashboard](https://database.new)

2. Clone the repository 

   ```bash
   # Using Git
    git clone https://github.com/your-repo/mvp-template.git
   ```


3. Install dependencies

   ```bash
    cd mvp-template
    pnpm install 
   ```

4. Rename `.env.example` to `.env.local` and update the following:

   ```
   NEXT_PUBLIC_SUPABASE_URL=[INSERT SUPABASE PROJECT URL]
   NEXT_PUBLIC_SUPABASE_ANON_KEY=[INSERT SUPABASE PROJECT API ANON KEY]
   ```

   Both `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY` can be found in [your Supabase project's API settings](https://app.supabase.com/project/_/settings/api)

5. You can now run the Next.js local development server:

   ```bash
   npm run dev
   ```

   The starter kit should now be running on [localhost:3000](http://localhost:3000/).
  

6. This template comes with the default shadcn/ui style initialized. If you instead want other ui.shadcn styles, delete `components.json` and [re-install shadcn/ui](https://ui.shadcn.com/docs/installation/next)

   ```bash
   rm components.json
   pnpm dlx shadcn@latest init
   ```



