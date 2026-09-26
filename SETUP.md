# MSK Gallery CMS Setup — Next Steps

## You have committed:

✅ package.json — dependencies configured
✅ tsconfig.json — TypeScript configured
✅ next.config.js — Next.js config with Cloudinary support
✅ .env.example — environment template
✅ payload.config.ts — Payload CMS configuration
✅ collections/Users.ts — admin authentication
✅ collections/Artworks.ts — gallery artwork collection
✅ collections/Artists.ts — artist profiles
✅ collections/Crews.ts — crew profiles
✅ collections/Stories.ts — historical stories
✅ collections/Comments.ts — moderated comments
✅ .gitignore — standard Node/Next exclusions

## To continue locally:

### 1. Clone and install
```bash
git clone https://github.com/williamortiz/MSK.git
cd MSK
git checkout dev/gallery-cms
npm install
```

### 2. Set up PostgreSQL

Option A: Local Postgres
```bash
# Install Postgres locally, then create a database
createdb msk_gallery
```

Option B: Supabase (recommended for production)
- Go to https://supabase.com
- Create a new project
- Copy the PostgreSQL connection string to `.env.local`

### 3. Configure environment
```bash
cp .env.example .env.local
# Edit .env.local with your Postgres URL and Cloudinary credentials
```

### 4. Run migrations
```bash
npm run payload
# This initializes the database with Payload collections
```

### 5. Start dev server
```bash
npm run dev
# Visit http://localhost:3000/admin
# Create an admin user when prompted
```

### 6. Next CMS features to build

Once the server starts:
- Create the admin dashboard UI
- Build the homepage with Next.js
- Build `/gallery` page with grid and filters
- Build `/gallery/[slug]` detail page
- Build `/admin` content management interface
- Add image upload to Cloudinary
- Add comment moderation
- Add social share buttons
- Deploy to Vercel

## Important notes

- The database schema is defined in the Payload collections
- All admin content is managed at `/admin`
- Images should be uploaded through Cloudinary
- Comments need approval before display
- The site uses Google Analytics ID: `G-66XVZFXWMM`

When you're ready to continue, start by running the local dev server and creating admin users in Payload.
