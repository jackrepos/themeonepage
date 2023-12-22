# Developers

## Project Setup

```sh
npm create vite@latest
npm install vue-router@4

npm install
# Local server
npm run dev
# Build for production
npm run build
# To deploy on github. If there is a custom domain added to github then you need to download the CNAME file (in public folder if needed) that github automatically create and push in the branch into /dist
npm run build && npm run deploy

# before deploying, add `"deploy": "gh-pages -d dist"` to `package.json`
npm install gh-pages --save-dev
```

- To add Bootstrap
Create folder `css` in `public`.
Move `bootstrap.min.css` to the `css` folder.
Add line `<link href="/css/bootstrap.min.css" rel="stylesheet">`

- To create new page
Create html `policy.html`, then create `policy.ts` then `Policy.vue`

## Inspirations

<https://www.dentistealaval.com/en/#>
<https://www.dentistealaval.com/en/cerec-crown/>
<https://www.dentistealaval.com/en/financing/>
<https://www.dentistealaval.com/en/appointment/>
<https://www.dentistealaval.com/en/privacy-policy/>

