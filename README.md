# Testimonials Slider 💬

A modern, responsive, and lightweight testimonial slider built with vanilla HTML5, CSS3, and JavaScript. The component automatically cycles through client testimonials, displaying user avatars, quotes, and names with timed transitions.

---

## 🌟 Features

- **Automatic Slider:** Seamlessly transitions between client reviews on a set interval.
- **Modern UI Design:** Clean card layout with floating circular avatar images and custom typography.
- **Pure Vanilla Stack:** Zero dependencies or external libraries (no jQuery, React, or Bootstrap needed).
- **Responsive & Flexible:** Adapts to desktop, tablet, and mobile viewport sizes.
- **Easily Extensible:** Simple data array in `script.js` allows quick addition or modification of testimonials.

---

## 📁 Project Structure

```text
Testimonials_slider/
│
├── index.html       # HTML structure for the testimonial card
├── style.css        # Card layout, typography, avatar styling, and colors
├── script.js        # Testimonials data source and automatic sliding logic
└── README.md        # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

All you need is any modern web browser (Google Chrome, Firefox, Safari, Edge).

### Running Locally

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Testimonials_slider
   ```

2. **Open the project:**
   - Double-click `index.html` to open it directly in your default browser.
   - Or, if you use VS Code, right-click `index.html` and select **"Open with Live Server"**.

---

## ⚙️ How It Works

1. **Data Source:** An array of testimonial objects in `script.js` contains the client's `name`, `photoUrl`, and `text`.
2. **DOM Update:** The `updateTestimonial()` function extracts data using destructuring and updates the image source and text elements in the DOM.
3. **Timer Loop:** `setTimeout()` recursively triggers `updateTestimonial()` at a specified interval, cycling back to the beginning once all testimonials have been displayed.

---

## 🎨 Customization

To add your own testimonials, open `script.js` and add an object to the `testimonials` array:

```javascript
{
  name: "Your Client Name",
  photoUrl: "https://example.com/avatar.jpg",
  text: "Your client's feedback goes here..."
}
```

To adjust the transition interval, modify the timeout value at the bottom of `script.js` (e.g., `4000` for 4 seconds):

```javascript
setTimeout(() => {
  updateTestimonial();
}, 4000);
```

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
