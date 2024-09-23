# Digital Clock

A simple **Digital Clock** created using **HTML**, **CSS**, and **JavaScript**. This project displays the current time and updates every second. The clock can be styled using custom CSS, making it easy to modify the look and feel.

## Features

- Displays the current time in **HH:MM:SS** format.
- Automatically updates every second.
- Basic styling with CSS (customizable).
- Responsive design for different screen sizes.

## Demo

You can check out the live demo of the digital clock here: [Digital Clock Demo](#) _(Replace this link with your GitHub Pages or hosted link if available)_

## Technologies Used

- **HTML**: The structure of the clock.
- **CSS**: Styling the clock (e.g., fonts, colors, layout).
- **JavaScript**: Logic to update the time every second.

## Project Setup

1. **Clone the repository**:

   ```bash
   git clone https://github.com/AkshayTiwari27/digital-clock.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd digital-clock
   ```

3. **Open the `index.html` file in your browser** to view the digital clock.

## Code Explanation

### HTML (`index.html`)
The HTML provides the basic structure of the clock. A simple `div` is used to display the time.

```html
<div id="clock">
  <span id="hours"></span>:<span id="minutes"></span>:<span id="seconds"></span>
</div>
```

### CSS (`style.css`)
The CSS adds the styling for the clock, including fonts, layout, and colors.

```css
#clock {
  font-family: 'Arial', sans-serif;
  color: #333;
  font-size: 48px;
  text-align: center;
  margin-top: 20%;
}
```

### JavaScript (`script.js`)
The JavaScript handles the logic for fetching the current time and updating the DOM every second.

```javascript
function updateTime() {
  const now = new Date();
  const hours = String(now.getHours()).padStart(2, '0');
  const minutes = String(now.getMinutes()).padStart(2, '0');
  const seconds = String(now.getSeconds()).padStart(2, '0');
  
  document.getElementById('hours').textContent = hours;
  document.getElementById('minutes').textContent = minutes;
  document.getElementById('seconds').textContent = seconds;
}

setInterval(updateTime, 1000);
updateTime(); // Initial call to display time immediately
```

## Customization

- You can easily modify the appearance of the clock by editing the `style.css` file.
- Change the time format (12-hour or 24-hour) by adjusting the logic in `script.js`.
- Add additional features such as:
  - Displaying AM/PM for a 12-hour format.
  - Adding a date display.
  - Using different fonts or animations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue if you have suggestions for improving the project.
