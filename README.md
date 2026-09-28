# Web-Lab2

## File Organization

- index.html: the main page. It has 6 divs (A to F) with the class "box".
- styleA.css: Version A. The boxes are stacked vertically and centered with flexbox.
- styleB.css: Version B. Boxes A-E are side by side in the top left corner and box F is in the bottom right corner.

To see the other version, change the href in the link tag in index.html from styleA.css to styleB.css.

## Challenges

- In Version B there was more than 10px of space between the boxes. I found out that inline-block elements act like text, so the spaces between the divs in the HTML were also showing up. I fixed it with font-size: 0 on the body and font-size: 40px on the boxes.
- The styles for the last box didn't work when I opened the page with Live Server. Live Server adds a script tag at the end of the body, so box F was not the last child anymore. I used :last-of-type instead of :last-child.
- In Version A the boxes got smaller when I made the window short. Flex items shrink by default, so I added flex-shrink: 0.
- In Version B the padding and the border made the boxes bigger than 100x150. I used box-sizing: border-box to keep them at the right size.