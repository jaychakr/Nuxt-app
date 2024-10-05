## SEO (Search Engine Optimization) and Analytics

Lesson 7 focuses on social tags, SEO, and analytics tools to enhance website visibility and user engagement. Social tags, like Facebook and Twitter share buttons, simplify content sharing on social media, while meta tags control how links appear. SEO (Search Engine Optimization) involves using strategies like single H1 tags, quality backlinks, and avoiding hidden text to improve search engine rankings and drive organic traffic. Key Performance Indicators (KPIs) help measure the effectiveness of your website, guiding development choices based on user behavior.

Utilizing tools like Google Analytics provides insights into user interactions, and heat maps can visualize engagement with content. For further learning, resources like Moz and insights from Rand Fishkin can deepen your understanding of SEO best practices. Overall, effectively combining these elements can significantly boost your website’s reach and success.

## SEO Proposal

In order to ideally implement SEO on the site:
- Match content to user searches using HTML header tags (h1, h2, h3, h4, h5, h6), using only one h1 tag per page. The h1 tags that could be used on each index.vue file within the pages/ directory are Bootstrap Accordion, REST Countries API Africa, REST Countries API America, Responsive Bootstrap Images, v-model Directive, Coat of Arms, and Landing Page.
- Avoid hiding text using the CSS display property and the value none (display: none). One possibility is to generate individual detailed descriptions for each country that could be included in each Card component. These descriptions would be visible similar to the other data points.
  Code samples could also be used to help the viewer better understand the Vue or Bootstrap functionality underlying each UI interaction.
- Include quality backlinks to relevant and reputable sites. Adding links to the Wikipedia page for each country would be appropriate. Links to YouTube videos of the soccer teams for each country are another option. Dynamic routing could be used to pass in each country name as a variable
  and then append it to the relevant URL.

# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install the dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm run dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm run build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm run preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
