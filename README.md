# Jaunsen - astro + storyblok website

## Roadmap

- [ ] Add Storyblok CMS
- [ ] Adapt to Netlify & deploy
- [ ] Customize with existing resources
- [ ] if good deploy to prod domain
- [ ] Clean up code from unecessary dependencies (Vue, Tailwind, etc)

# Astrogency | Astro Agency Template | Storyblok CMS

### 👉 [Demo & Docs](https://astrogency.unfolding.io/)

## 📝 1. Setting up the .env file

rename the `env.txt` to `.env` and fill in your details

```
STORYBLOK_PREVIEW_TOKEN=XXX
STORYBLOK_PERSONAL_TOKEN=XXX
STORYBLOK_SPACE_ID=000000
STORYBLOK_REGION=eu
LOCALE=en-US
CURRENCY=USD
SITE_LANG=en
```

Also add this to your netlify/vercel deploy settings.

### 🧰 2. Install dependencies

```bash
npm install
```

### 🛠️ 3. Start Development server

```bash
npm run dev
```

### 🔄 4. Sync your Storyblok Space

open `https://localhost:4321/setup`

And sync your Datasources, Components, and stories. it is best to first delete before syncing.
_if a sync or delete fails, try to refresh the page ant try again._

![Astrorante](https://astrorante.unfolding.io/screenshots/sync.png)

### ⚙️ 5. Add your site to the astro.config and set your adapter (vercel or netlify)

```javascript

export default defineConfig({
	site: 'https://your-website.com',
	output: "hybrid",
  	adapter: vercel(), // vercel() or netlify()
	...
})

```

## 🛸 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| ------------------------- | ------------------------------------------------ |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CL                      |

## 📚 Tech Stack

Astro, Storyblok CMS, Vue, TailwindCSS
