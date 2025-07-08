# Coffee Blog

## Description
A simple responsive gallery page dedicated to Dublin's cafes and coffee life—from brewing methods and coffee origins to gear reviews and tips. Readers can subscribe via a signup form to receive updates.

It is the three page website: home, gallery and and a sign-up page. In the future, the blog page will posts will be added. 

## Goal
The page is to showcase Dublin's vibrant coffee scene by showcasing a gallery of photos

## Features
- Blog index and individual post pages
- Newsletter signup form using [the codeinstitiute dumpti](https://formdump.codeinstitute.net)
- Mobile-first and accessible design
- Easy to deploy on GitHub Pages

## Tech Stack
- HTML, CSS, JavaScript

## Media
Most of the images used comes from my own library. However, there are a few exeptions:
* Hero image named "pexels-emrecan-2079438" on the home page was created by [Emre Can Acer](https://www.pexels.com/photo/lighted-pendant-lights-inside-bar-2079438) and found originally on Pexels; 
* Image named "pexels-apgpotr-683039" in the Assets folder was created by [Afta Putta Gunawan
Afta Putta Gunawan](https://www.pexels.com/photo/assorted-decors-with-brown-rack-inside-store-683039/);
* Image named "pexels-fotios-photos-1024359" in the Assets folder, but not used, was created by [Lisa from Pexels](https://www.pexels.com/photo/pink-rose-in-vase-centerpiece-on-brown-wooden-table-1024359/);
* My Favicon icons were created in Canva using the "cute coffee" graphic by @heybas
* My image featuring a coffee bean in a cup on the table was created in Canva.It used the graphic by @tomodaging and the photo of the table by [Larisa Ghergh](https://www.gettyimages.ie/detail/photo/close-up-of-wooden-table-in-restaurant-royalty-free-image/1347320446) 
* Social media favicons were taken from https://fontawesome.com/.

## Fonts
I used two fonts from Google Fonts: [Lato and Lexend](https://fonts.google.com/share?selection.family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900|Lexend:wght@100..900). 

## Issues and Solutions
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