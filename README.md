## README for Animated Wavy Background Project

### Project Overview

This project demonstrates a simple web page with an animated wavy background and a centered card displaying product information. The animation creates a visually appealing effect for the background, making it ideal for use in various web design projects.

### Features

- **Animated Wavy Background:** A smooth, wavy animation applied to the background.
- **Centered Card Layout:** A card positioned at the center of the page with a product title and description.
- **Responsive Design:** Ensures the layout adapts to different screen sizes.

### Technologies Used

- **HTML**
- **CSS**

### File Structure

```
project-root/
├── index.html
└── style.css
```

### HTML Code

The `index.html` file contains the structure of the web page. Here's the content:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animated Wavy Background</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>
  <div class="page">
    <div class="card">
      <div class="product">
        <h2>Product</h2>
      </div>
      <div class="details">
        <h4>Card Title</h4>
        <p>Description</p>
      </div>
    </div>
  </div>
</body>

</html>
```

### CSS Code

The `style.css` file contains the styles and animations for the web page. Here's the content:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

.page {
  position: relative;
  width: 100vw;
  height: 100vh;
}

.card {
  z-index: 100;
  display: flex;
  flex-direction: column;
  position: absolute;
  width: 40vw;
  min-width: 270px;
  height: 40vh;
  min-height: 400px;
  background-color: #eee;
  top: 50%;
  left: 50%;
  border-radius: 0.5rem;
  transform: translate(-50%, -50%);
  padding: 0.9rem;
}

.card .product {
  border-radius: 0.3rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #eee;
  background-color: #455456;
  flex-grow: 1;
}

.card .details {
  color: #455456;
  display: flex;
  flex-direction: column;
  padding: 0.9rem 0.3rem;
  align-items: center;
}

.card .details p {
  font-size: 13px;
}

.page::before {
  z-index: -10;
  content: "";
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) skew(0deg, -10deg);
  border-radius: 50%;
  width: 230%;
  height: 210%;
  background-color: #0099ff;
  animation: backAnimation ease alternate 7s infinite;
}

@keyframes backAnimation {
  0% {
    transform: translateX(-50%) skew(0deg, -10deg);
  }
  100% {
    transform: translateX(-30%) skew(30deg, 0deg);
  }
}
```

### Getting Started

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   ```
2. **Navigate to the project directory:**
   ```bash
   cd project-directory
   ```
3. **Open `index.html` in your browser to view the application.**

### Usage

- Open the web page to see the animated wavy background and centered card.
- The animation and card layout should adapt to different screen sizes, providing a responsive design.

### License

This project is licensed under the MIT License.

For any further details or contributions, please refer to the project repository.
