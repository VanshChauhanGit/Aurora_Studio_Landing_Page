# Aurora Studio Responsive Website

This project is a 3-page, fully responsive, and accessible company landing site for "Aurora Studio". It is built using only HTML and CSS, as per the project requirements.

---

## How to Open the Site

1.  Unzip the project folder.
2.  Ensure all files and folders (`index.html`, `about.html`, `contact.html`, `css/style.css`) are in the same directory.
3.  Open the `index.html` file in any modern web browser (e.g., Chrome, Firefox, Safari, Edge) to start or open the project folder in any code editor (e.g., Visual Studio Code) and then run the `index.html` file.
4.  You can navigate to the other pages using the links in the header and footer.

---

## CSS-Only Techniques Used

### 1. Responsive Mobile Navigation (Checkbox Hack)

- **How it works:**
  - A visually-hidden `input[type="checkbox"]` (`.nav-toggle`) is placed in the header.
  - A visible `<label>` (`.nav-toggle-label`) is associated with the checkbox using the `for` attribute. This label contains the hamburger/close icons.
  - Clicking the label toggles the checkbox's `:checked` state.
  - The navigation menu (`.main-nav`) is positioned absolutely and hidden using `max-height: 0` and `overflow: hidden`.
  - A CSS sibling selector (`.nav-toggle:checked ~ .main-nav`) targets the navigation menu when the checkbox is checked, animating its `max-height` to a large value (100vh) to slide it into view.

### 2. Image Gallery Lightbox (:target Hack)

- **How it works:**
  - Each gallery thumbnail links to a specific hash ID (e.g., `href="#img1"`).
  - Hidden `<a>` tags with corresponding IDs (e.g., `id="img1"`) are placed at the end of the `index.html` file. These `<a>` tags act as the lightbox overlay and are hidden by default with `display: none`.
  - When a thumbnail is clicked, the URL hash changes, and the corresponding `<a>` tag becomes the `:target` of the page.
  - The CSS rule `.lightbox:target` applies `display: flex` to the targeted lightbox, making it visible as a modal overlay.

---

## Known Issues

None at this time. The site has been tested for responsiveness, accessibility (keyboard navigation, skip links, semantic HTML), and print-friendliness.

---

## Credits

- **Fonts:** Inter and Roboto Slab via Google Fonts.
- **Icons:** Font Awesome (CDN).
- **Images:** Placeholder images from [Placehold](https://placehold.co/).
