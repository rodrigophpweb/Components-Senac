# Countdown Component

This repository contains a simple countdown component implemented in HTML, CSS, and JavaScript. The countdown timer calculates the remaining time until a target event date and dynamically displays the days, hours, minutes, and seconds remaining. This component also includes an animated design and custom styles to enhance the visual appeal.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Technologies](#technologies)
- [License](#license)

## Features

- **Dynamic Countdown**: Displays days, hours, minutes, and seconds remaining until the target date.
- **Responsive Design**: Automatically adjusts to fit different screen sizes.
- **Animations**: Includes hover effects, smooth transitions, and subtle animations such as pulse and flip effects.
- **Custom Styling**: Includes a vibrant color scheme with a linear gradient separator, rounded corners, shadows, and text effects.
- **Event-Specific**: Configured to countdown to an event happening on May 24, 2025.

## Installation

No installation is required for this component. Simply copy the HTML, CSS, and JavaScript code and integrate it into your project.

Alternatively, you can clone this repository to get the files locally:

```bash
git clone https://github.com/your-username/countdown-component.git
```

Then, open the index.html file in your browser to see the countdown in action.

## Usage

To use this countdown component in your project:

1. **HTML**: Integrate the countdown HTML structure into your webpage.
2. **CSS**: Copy the provided CSS into your stylesheets for the animated and styled elements.
3. **JavaScript**: Include the script to handle the countdown logic. You can modify the target date within the script.

## Example HTML Structure

```html
<div class="container">
  <img src="path-to-logo.png" alt="Event Logo">
  <div class="separator"></div>
  <div class="countdown">
    <div><span id="days"></span><div class="time-label">Days</div></div>
    <div><span id="hours"></span><div class="time-label">Hours</div></div>
    <div><span id="minutes"></span><div class="time-label">Minutes</div></div>
    <div><span id="seconds"></span><div class="time-label">Seconds</div></div>
  </div>
  <mark class="date-text">24 and 25 of May, 2025</mark>
</div>
```
## Example JavaScript for Countdown

```javascript
function updateCountdown() {
  const targetDate = new Date('May 24, 2025 09:00:00').getTime();
  const now = new Date().getTime();
  const timeLeft = targetDate - now;

  const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
  const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

  document.getElementById('days').innerHTML = days;
  document.getElementById('hours').innerHTML = hours;
  document.getElementById('minutes').innerHTML = minutes;
  document.getElementById('seconds').innerHTML = seconds;
}

setInterval(updateCountdown, 1000);
```
## Customization

You can easily customize the countdown by:

- **Changing the Target Date**: Modify the date in the JavaScript 'targetDate' to match your event.
- **Styling**: Adjust colors, fonts, animations, and layout through the CSS to fit your design preferences.
- **Event Logo**: Replace the image URL to include your custom event logo.

### Changing the Target Date

To adjust the countdown for your event, change the date in this section of the JavaScript:

```javascript
const targetDate = new Date('Your Event Date Here').getTime();

## Technologies

- **HTML**: Structure of the countdown component.
- **CSS**: Provides styling and animations, including the custom separator gradient and pulse effects.
- **JavaScript**: Handles the countdown logic and dynamic updates to the display.

#License
This project is open-source and available under the MIT License. Feel free to modify and use it in your projects.
