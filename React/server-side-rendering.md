#### Server Side Render (SSR)

* A technique where the HTML for a page is generated on the server rather than on the client
* The advantages of this approach:
  * faster initial load times
  * better Search Engine Optimization (SEO)
  * can provide a smoother user experience
* SSR can be achieved using frameworks like Next.js
  * simplify setting up SSR and other rendering strategies

#### How Server-Side Rendering Works
* Traditional client-rendered React app
  * JavaScript code is downloaded to the browser
  * Browser executes JS to generate HTML and renders content
  * User may see blank page initially
  * May take a few moments for the content to appear, especially on slower networks
* SSR
  * The React app runs on the server and generates the full HTML page
  * The server sends this pre-rendered HTML to the client
  * The client can see the fully rendered page immediately, even before the JavaScript is loaded
  * React's JavaScript then 'hydrates' the page, making it interactive on the client side

#### Benefits of SSR
* SEO: Search engines can better index the content since they receive a fully rendered HTML page from the start
* Performance: Users see content faster because the server sends a complete HTML document
* User Experience: Avoids te 'flash of blank content' sometimes seen in client-side rendering
