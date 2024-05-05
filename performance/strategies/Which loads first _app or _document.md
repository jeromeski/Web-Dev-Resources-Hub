In Next.js, `_document.tsx` is loaded before `_app.tsx`. The `_document.tsx` file is used to augment the HTML `<Document>` structure that gets rendered server-side. It's only rendered on the server and is where you can add HTML attributes, custom fonts, or the `<head>` elements that are common across all pages¹.

On the other hand, `_app.tsx` is the custom App component that allows you to control the page initialization, and it wraps around all of your pages. It's where you can include global CSS and keep state between page navigations¹.

Here's the order in which they are loaded and used:
1. `_document.tsx` is rendered on the server to produce the initial HTML structure.
2. `_app.tsx` initializes the React application, wrapping all the page components and managing global state or styles.

It's important to note that `_document.tsx` does not re-render on client-side routing, but `_app.tsx` does. So, for any changes that need to persist across different pages, `_app.tsx` is the right place to make those changes¹.

Source: Conversation with Bing, 5/5/2024
(1) Routing: Custom Document | Next.js. https://nextjs.org/docs/pages/building-your-application/routing/custom-document.
(2) next.js - Confused about NextJS, whether to use "app"-directory or .... https://stackoverflow.com/questions/76385648/confused-about-nextjs-whether-to-use-app-directory-or-pages-and-index-tsx.
(3) Next.js use of _app.js and _document.js - Stack Overflow. https://stackoverflow.com/questions/51040669/next-js-use-of-app-js-and-document-js.
(4) javascript - In Next JS, changes in layout.tsx only applies to home .... https://stackoverflow.com/questions/77307474/in-next-js-changes-in-layout-tsx-only-applies-to-home-page-other-pages-are-not.
(5) Upgrading: From Pages to App | Next.js. https://nextjs.org/docs/pages/building-your-application/upgrading/app-router-migration.
(6) undefined. https://nextjs.org/docs.
(7) undefined. https://nextjs.org/docs/app/building-your-application/upgrading/app-router-migration.