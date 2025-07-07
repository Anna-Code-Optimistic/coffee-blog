# Coffee Blog

## Description
A simple responsive gallery page dedicated to Dublin's cafes and coffee life—from brewing methods and coffee origins to gear reviews and tips. Readers can subscribe via a signup form to receive updates.

## Features
- Blog index and individual post pages
- Mailchimp-based newsletter signup form
- Mobile-first and accessible design
- Easy to deploy on GitHub Pages

## Tech Stack
- HTML, CSS, JavaScript
- Optional: Jekyll or Eleventy for static site generation

### Issues and Solutions
I followed the Love Running project to help build my page. The structure is very similar, but I applied different fonts, a custom colour palette, and new imagery. I also added a comment box to the sign-up form.

On my homepage, when applying the background image, I initially attached it to this section:

   < main>
        < section id="hero">
            < div id="cover-text">
                < h2> Discover Dublin's Coffee Scene< /h2>
                < h3> Tap into local stories over a cup of coffee.< /h3>
            < /div>
     < /section>

However, the image wasn't stretching across the entire screen — it stayed within that section. To fix it, I applied the following styles:

    width: 100vw;
    height: 100vh;
    background: url("../images/pexels-emrecan-2079438.jpg") no-repeat center center/ cover;

I also realized that some image file names were causing issues. For example, they had capital letters, spaces, or used .JPG instead of .jpg. I renamed all image files to use lowercase letters and no spaces for consistency and compatibility. Then I updated the file paths to ensure the file names were displayed correctly.

When building the gallery, I initially used backslashes in the image paths like this: assets\images\proper-order-coffee-87.jpg. It happened because I copied relative paths. However, when using HTML Checker, the tool highlighted Backslash as a potential issue. I updated the paths to have forward slashes instead. 

I’m still building confidence with Flexbox and forms. I adapted the sample project template and customised the content, labels, colours, and values to suit my project. I added a comments box with placeholder text and used a < br > tag to add spacing between the main fields and the comments area.

In index.html, I applied < link rel="coffee-favicon" sizes="192x192" href="assets/favicon/Coffee-Favicon-192-x-192.png">. The HTM Checker gave me this error:  "A link element with a sizes attribute must have a rel attribute that contains the value icon or the value apple-touch-icon or the value apple-touch-icon-precomposed." So I corrected it to: "icon"

As my footer has a background colour, when applying favicons,  I wanted the social icons to contrast well. So I applied inline styles to change their colour directly in the HTML. < i class="fa-brands fa-facebook" style="color: #ffffff;">< /i><

I originally had a Blog page in my project but ultimately decided not to include it. After removing the related section from the project and the navigation bar across all the pages, I noticed that the "Blog" link was still showing in the browser preview and on my GitHub Page.

Even after doing a hard refresh (Ctrl + F5), the link remained visible. To double-check, I opened the site in Incognito mode, and confirmed that the "Blog" section was indeed removed from the current version of the project. This led me to realise that the issue was caused by browser caching. My regular browser session had cached the older version of the page, so the changes weren't appearing immediately. Incognito mode, which doesn't rely on the same cache, showed the updated page correctly.