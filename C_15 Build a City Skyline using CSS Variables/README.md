# City Skyline Webpage

## Overview

This project creates a city skyline with a background and foreground of buildings using HTML and CSS. The skyline features buildings with different colors and window styles, and the background changes based on the time of day to simulate morning and night effects.

## File Structure

- `index.html`: The HTML file defining the structure of the city skyline.
- `styles.css`: The CSS file containing styles for the buildings, windows, and background.

## Features
![Static Badge](https://img.shields.io/badge/HTML5-%23E34F26?style=for-the-badge&logo=HTML5&logoColor=white)
![Static Badge](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white)
![Static Badge](https://img.shields.io/badge/freecodecamp-0A0A23?style=for-the-badge&logo=freecodecamp&logoColor=white)
1. **Responsive Design**: The layout adjusts based on screen width.
2. **Day/Night Background**: Background color and gradient adjust to simulate light and dark conditions based on the screen width.

## HTML Structure

- **`.background-buildings`**: Container for background buildings.
  - `.bb1`, `.bb2`, `.bb3`, `.bb4`: Different types of background buildings with specific styles.
- **`.foreground-buildings`**: Container for foreground buildings.
  - `.fb1`, `.fb2`, `.fb3`, `.fb4`, `.fb5`, `.fb6`: Different types of foreground buildings with specific styles.

## CSS Details

### Colors

- **Building Colors**: Defined using CSS variables for easy adjustments.
- **Window Colors**: Also defined using CSS variables to maintain consistency.

### Background

- **Daytime (default)**: Radial gradient background simulating a sunny day.
  <div align="center">
  <img src="https://github.com/user-attachments/assets/60c20278-57e6-404f-be6d-47cea23d627a" alt="book list" width="500" />
</div>

- **Nighttime (when screen width is less than 1000px)**: Radial gradient background simulating nighttime.
<div align="center">
  <img src="https://github.com/user-attachments/assets/ab8c4298-7830-4533-9328-851c909ab449" alt="book list" width="400" />
</div>


### Responsive Design

When the screen width is less than `1000px`, the background changes to darker colors to simulate nighttime.

```css
@media (max-width: 1000px) {
  :root {
    --building-color1: #000;
    --building-color2: #000;
    --building-color3: #000;
    --building-color4: #000;
    --window-color1: #777;
    --window-color2: #777;
    --window-color3: #777;
    --window-color4: #777;
  }
  .sky {
    background: radial-gradient(
        closest-corner circle at 15% 15%,
        #ccc,
        #ccc 20%,
        #445 21%,
        #223 100%
      );
  }
}
