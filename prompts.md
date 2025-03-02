以下のエラーの原因を調査して、エラーを解消する方法と解消版の package.json を提示してください。

```shell
 ~/workspace/blogs/tailwind-nextjs-starter-blog [main] $ npm i
npm error code ERESOLVE
npm error ERESOLVE unable to resolve dependency tree
npm error
npm error While resolving: tailwind-nextjs-starter-blog@2.3.0
npm error Found: react@19.0.0
npm error node_modules/react
npm error   react@"19.0.0" from the root project
npm error
npm error Could not resolve dependency:
npm error peer react@"^16.8 || ^17 || ^18" from next-themes@0.3.0
npm error node_modules/next-themes
npm error   next-themes@"^0.3.0" from the root project
npm error
npm error Fix the upstream dependency conflict, or retry
npm error this command with --force or --legacy-peer-deps
npm error to accept an incorrect (and potentially broken) dependency resolution.
npm error
npm error
npm error For a full report see:
npm error /Users/zero/.npm/_logs/2025-03-01T15_33_38_346Z-eresolve-report.txt
npm error A complete log of this run can be found in: /Users/zero/.npm/_logs/2025-03-01T15_33_38_346Z-debug-0.log
```

```json:package.json
{
  "name": "tailwind-nextjs-starter-blog",
  "version": "2.3.0",
  "private": true,
  "scripts": {
    "start": "next dev",
    "dev": "cross-env INIT_CWD=$PWD next dev",
    "build": "cross-env INIT_CWD=$PWD next build && cross-env NODE_OPTIONS='--experimental-json-modules' node ./scripts/postbuild.mjs",
    "serve": "next start",
    "analyze": "cross-env ANALYZE=true next build",
    "lint": "next lint --fix --dir pages --dir app --dir components --dir lib --dir layouts --dir scripts",
    "prepare": "husky"
  },
  "dependencies": {
    "@headlessui/react": "2.2.0",
    "@next/bundle-analyzer": "15.1.4",
    "@tailwindcss/forms": "^0.5.9",
    "@tailwindcss/postcss": "^4.0.5",
    "@tailwindcss/typography": "^0.5.15",
    "body-scroll-lock": "^4.0.0-beta.0",
    "contentlayer2": "0.5.4",
    "esbuild": "0.20.2",
    "github-slugger": "^2.0.0",
    "gray-matter": "^4.0.2",
    "hast-util-from-html-isomorphic": "^2.0.0",
    "image-size": "1.0.0",
    "next": "15.1.4",
    "next-contentlayer2": "0.5.4",
    "next-themes": "^0.3.0",
    "pliny": "0.4.1",
    "postcss": "^8.4.24",
    "react": "19.0.0",
    "react-dom": "19.0.0",
    "reading-time": "1.5.0",
    "rehype-autolink-headings": "^7.1.0",
    "rehype-citation": "^2.0.0",
    "rehype-katex": "^7.0.0",
    "rehype-katex-notranslate": "^1.1.4",
    "rehype-preset-minify": "7.0.0",
    "rehype-prism-plus": "^2.0.0",
    "rehype-slug": "^6.0.0",
    "remark": "^15.0.0",
    "remark-gfm": "^4.0.0",
    "remark-github-blockquote-alert": "^1.2.1",
    "remark-math": "^6.0.0",
    "tailwindcss": "^4.0.5",
    "unist-util-visit": "^5.0.0"
  },
  "devDependencies": {
    "@eslint/eslintrc": "^3.2.0",
    "@eslint/js": "^9.16.0",
    "@svgr/webpack": "^8.0.1",
    "@types/mdx": "^2.0.12",
    "@types/react": "^19.0.8",
    "@typescript-eslint/eslint-plugin": "^8.12.0",
    "@typescript-eslint/parser": "^8.12.0",
    "cross-env": "^7.0.3",
    "eslint": "^9.14.0",
    "eslint-config-next": "15.1.4",
    "eslint-config-prettier": "^9.1.0",
    "eslint-plugin-prettier": "^5.2.0",
    "globals": "^15.12.0",
    "husky": "^9.0.0",
    "lint-staged": "^13.0.0",
    "prettier": "^3.0.0",
    "prettier-plugin-tailwindcss": "^0.6.11",
    "typescript": "^5.1.3"
  },
  "lint-staged": {
    "*.+(js|jsx|ts|tsx)": [
      "eslint --fix"
    ],
    "*.+(js|jsx|ts|tsx|json|css|md|mdx)": [
      "prettier --write"
    ]
  },
  "packageManager": "yarn@3.6.1"
}
```