# Next.js Tutorial

The Next.js is React Based framework with server side rendering capability. It is very fast and SEO friendly.

Using Next.js, you can create robust react based application quite easily and test them. Following are the key features of Next.js.

Hot Code Reload − Next.js server detects modified files and reloads them automatically.

Automatic Routing − No need to configure any url for routing. files are to be placed in pages folder. All urls will be mapped to file system. Customization can be done.

Component specific styles − styled-jsx provides support for global as well as component specific styles.

Server side rendering − react components are prerendered on server hence loads faster on client.

Node Ecosystem − Next.js being react based gels well with Node ecosystem.

Automatic code split − Next.js renders pages with libraries they need. Next.js instead of creating a single large javascript file, creates multiples resources. When a page is loaded, only required javascript page is loaded with it.

Prefetch − Next.js provides Link component which is used to link multiple components supports a prefetch property to prefetch page resources in background.

Dynamic Components − Next.js allows to import JavaScript modules and React Components dynamically.

Export Static Site − Next.js allows to export full static site from your web application.

Built-in Typescript Support − Next.js is written in Typescripts and provides excellent Typescript support.

In Next.js, we can create pages and navigate between them using file system routing feature. We'll use Link component to have a client side navigation between pages.

In Next.js, a page is a React Component and are exported from pages directory. Each page is associated with a route based on its file name. For example

pages/index.js is linked with '/' route.

pages/posts/first.js is linked with '/posts/first' route and so on.

Create post directory and first.js within it with following contents.
```
export default function FirstPost() {
   return <h1>My First Post</h1>
}
```
Add Link Support to go back to Home page. Update first.js as follows −
```
import Link from 'next/link'

export default function FirstPost() {
   return (
      <>
         <h1>My First Post</h1>
         <h2>
            <Link href="/">
               <a>Home</a>
            </Link>
         </h2>
      </>	  
   )
}
```
Add Link Support to home page to navigate to first page. Update index.js as follows −
```
import Link from 'next/link'

function HomePage() {
   return (
      <>
         <div>Welcome to Next.js!</div>
         <Link href="/posts/first"><a>First Post</a></Link>
      </>	    
   )
}

export default HomePage
```

In Next.js, we can serve static pages like images very easily by putting them in public, a top level directory. We can refer these files in similar fashion like pages in pages directory.

In Next.js, a page is a React Component and are exported from pages directory. Each page is associated with a route based on its file name.

Let's update the nextjs project used in Pages chapter.

Create public directory and place any images within it. We've taken logo.png, TutorialsPoint Logo image.

```
import Link from 'next/link'

export default function FirstPost() {
   return (
      <>
         <h1>My First Post</h1>
         <h2>
            <Link href="/">
               <a>Home</a>
            </Link>
         </h2>
         <br/">
         <img src="/logo.png" alt="TutorialsPoint Logo" />
      </>	  
   )
}
```
