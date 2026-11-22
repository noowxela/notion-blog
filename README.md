This is a [Next.js](https://nextjs.org/) blog using [Notions Public API](https://developers.notion.com).

__Demo:__ [https://notion-blog-mu-peach.vercel.app/](https://notion-blog-mu-peach.vercel.app/)

__How-it-works/Documentation:__ [TBC](#)

## Getting Started

First, follow Notions [getting started guide](https://developers.notion.com/docs/getting-started) to get a `NOTION_TOKEN` and a `NOTION_DATABASE_ID`, then add them to a file called `.env.local`.

U can go see the latest notion integration process
https://www.notion.so/profile/integrations

u can getting u notion secret token by creating a intergation instance.
https://developers.notion.com/docs/create-a-notion-integration#create-your-integration-in-notion

As a reference here's the Notion table I am using: https://www.notion.so/177b5fd4cdf78038a96ecfaa9731869e?v=a60302e22eb240a481fe2a34b0bd4909

```
NOTION_TOKEN=
NOTION_DATABASE_ID=
```

Install dependencies

```bash
npm install
# or
yarn
```

Start the server with

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

#### Deploy to vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fsamuelkraft%2Fnotion-blog-nextjs&env=NOTION_TOKEN,NOTION_DATABASE_ID&envDescription=Please%20add%20NOTION_TOKEN%20and%20NOTION_DATABASE_ID%20that%20is%20required%20to%20connect%20the%20blog%20to%20your%20notion%20account.&envLink=https%3A%2F%2Fdevelopers.notion.com%2Fdocs%2Fgetting-started&project-name=notion-blog-nextjs&repo-name=notion-blog-nextjs&demo-title=Notion%20Blog%20Next%20JS&demo-description=%20This%20is%20a%20Next.js%20blog%20using%20Notions%20Public%20API.&demo-url=notion-blog-nextjs-coral.vercel.app)

#### GitHub Actions
- Deployment workflows are located under `.github/workflows/` in this repository.
- To use the actions, rename them to remove the `.txt` extensions


To be able to deploy on both vercel and gh pages through GitHub actions when merging/pushing to master, add the following as your GitHub Action Secrets (Settings->Secrets->Actions).
1. ORG_ID - Vercel account ID found in account Settings.
1. PROJECT_ID - Vercel project ID found in project Settings.
1. VERCEL_TOKEN - Vercel token created in Settings -> Tokens.
1. GH_TOKEN - GitHub token usually readily available for each account (optional).