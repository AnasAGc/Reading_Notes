# React 3
## Assets
### Assets
#### Next.js can serve static assets, like images, under the top-level `public` directory. Files inside `public` can be referenced from the root of the application similar to pages The `public` directory is also useful for `robots.txt`, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.
### Image Component and Image Optimization
#### next/image is an extension of the HTML `<img>` element, evolved for the modern web.`Next.js` also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it
### Using the Image Component
#### Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.
## CSS Styling
### CSS Styling
#### If you take a look at pages/index.js, you should see code like this:
```
<style jsx>{`
  …
`}</style>
```
#### This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped. Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.
### Writing and Importing CSS
#### `Next.js` has built-in support for CSS and Sass which allows you to import .css and .scss files. Using popular CSS libraries like Tailwind CSS is also supported.
### Layout Component
#### we can create a Layout component that can be shared across all pages
### Adding CSS
#### To add some styles to the Layout component, we’ll use CSS Modules, which lets us import CSS files in a React component. Important: To use CSS Modules, the CSS file name must end with `.module.css`.
### Automatically Generates Unique Class Names
#### what CSS Modules does is automatically generates unique class names. As long as you use CSS Modules, so you don’t have to worry about class name collisions.Furthermore, `Next.js`’s code splitting feature works on CSS Modules as well. It ensures the minimal amount of CSS is loaded for each page. This results in smaller bundle sizes
### Global Styles
#### CSS Modules are useful for component-level styles. But if you want some CSS to be loaded by every page, Next.js has support for that as well.
### Styling Tips
#### some styling tips that might be helpful:
- Using `classnames` library to toggle classes
- Customizing PostCSS Config
- Using Sass