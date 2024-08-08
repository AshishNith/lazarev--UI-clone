# Practice Project

This project is a simple practice project to create a webpage with a navigation menu, a main section with animated elements, and a footer using HTML, CSS, and JavaScript.

## Features

1. **Fixed Navigation Bar**: 
    - Includes the title "LAZAREV."
    - A navigation section with multiple elements.
    - A button with an SVG icon that says "Let's Talk."

2. **Animated Main Section**: 
    - Contains a title with an SVG icon.
    - A paragraph with sample text.
    - A section showcasing services offered, like brand design, user experience, and digital product design.
    - A moving div with logos of various companies.

3. **GSAP Animations**: 
    - The navigation elements expand when hovered over using GSAP (GreenSock Animation Platform).
    - Moving div animations for a smooth scrolling effect.

## File Structure

- `index.html`: The main HTML file containing the structure of the webpage.
- `style.css`: The CSS file for styling the webpage.
- `script.js`: The JavaScript file for adding interactivity and animations.
- `favicon.ico`: The favicon for the webpage.

## Technologies Used

- HTML5
- CSS3
- JavaScript
- GSAP (GreenSock Animation Platform)

## How to Use

1. **Clone the Repository**:
    ```bash
    git clone <repository-url>
    ```
2. **Navigate to the Project Directory**:
    ```bash
    cd practice-project
    ```
3. **Open the `index.html` File**:
    Open the `index.html` file in your preferred web browser to see the webpage in action.

## Customization

You can customize the content of the webpage by modifying the `index.html`, `style.css`, and `script.js` files. Below are some customization options:

- **Change Titles and Text**:
  Update the text within the HTML elements to reflect your own content.

- **Modify Styles**:
  Edit the CSS classes in the `style.css` file to change the appearance of the webpage.

- **Add/Remove Navigation Elements**:
  Add or remove `nav-elem` elements in the HTML file to customize the navigation menu.

- **Change Animation Effects**:
  Modify the GSAP animations in the `script.js` file to create different animation effects.

## Example Usage

Here is an example of how the navigation bar expands on hover using GSAP:

```javascript
var nav = document.querySelector("nav");

nav.addEventListener("mouseenter", function() {
    let tl = gsap.timeline();
    tl.to(".nav-bottom", {
        height: "21vh",
        duration: 0.05
    });
    tl.to(".nav-part2 h5", {
        display: "block"
    });
    tl.to(".nav-part2 h5 span", {
        y: 0,
        duration: 0.3,
        stagger: {
            amount: 0.5
        }
    });
});

nav.addEventListener("mouseleave", function() {
    let tl = gsap.timeline();
    tl.to(".nav-part2 h5 span", {
        y: 25,
        stagger: {
            amount: 0.2
        }
    });
    tl.to(".nav-part2 h5", {
        display: "none",
        duration: 0.1
    });
    tl.to(".nav-bottom", {
        height: "0vh",
        duration: 0.1
    });
});
