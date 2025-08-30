# Emergency Hotline Project

## Project Overview
Emergency Hotline is a web application that provides a directory of important emergency service numbers for quick access. The project aims to help users easily find and call government and other emergency services in Bangladesh.

## Features
- Interactive emergency service cards with icons, names, and numbers
- Call functionality with coin deduction system
- Copy phone numbers to clipboard
- Heart button to show likes
- Call history with timestamps and clear history option
- Responsive design for mobile and desktop

## Technologies Used
- HTML5
- CSS3 (with responsive design)
- JavaScript (ES6+)
- Font Awesome for icons

## Usage
1. Open `index.html` in a modern web browser.
2. Browse the emergency service cards.
3. Click the "Call" button to simulate a call (requires sufficient coins).
4. Click the "Copy" button to copy the phone number to clipboard.
5. Use the heart icon to like a service.
6. View and clear call history in the sidebar.

## Project Structure
- `index.html`: Main HTML file
- `styles.css`: Styling for the application
- `script.js`: JavaScript logic and interactivity
- `assets/`: Images and icons used in the project

## JavaScript Concepts Used in This Project

### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

**getElementById**: Returns a single element object that has the specified ID. It's the fastest method since IDs should be unique in the DOM. Used in this project to get elements like heart-count, coin-count, etc.

**getElementsByClassName**: Returns a live HTMLCollection of all elements that have the specified class name. It updates automatically if the DOM changes. Useful for selecting multiple elements with the same class.

**querySelector**: Returns the first element that matches a specified CSS selector string. It's versatile and can select by ID, class, tag, attribute, etc. Used in this project for more complex selections.

**querySelectorAll**: Returns a static NodeList of all elements matching the specified CSS selector string. Unlike getElementsByClassName, it does not update automatically. Good for selecting multiple elements with complex selectors.

### 2. How do you create and insert a new element into the DOM?

To create and insert a new element:
1. Use `document.createElement(tagName)` to create the element
2. Set attributes, classes, or content on the new element
3. Use methods like `appendChild()`, `insertBefore()`, or `replaceChild()` on a parent node

In this project, we use this pattern in the `renderCards()` function to dynamically create emergency service cards and in `renderHistory()` to display call history items.

### 3. What is Event Bubbling and how does it work?

Event Bubbling is a type of event propagation where an event starts from the deepest target element and then bubbles up to its ancestors in the DOM tree. For example, if you click a button inside a div, the click event triggers on the button first, then on the div, then on its parent elements up to the document.

This allows event handlers on parent elements to catch events from their children. In this project, we use event bubbling in the `setupEventListeners()` function where we listen for events on the document and then check which specific element was clicked.

### 4. What is Event Delegation in JavaScript? Why is it useful?

Event Delegation is a technique where a single event listener is added to a parent element to handle events for its child elements. Instead of attaching event listeners to multiple child elements, you listen on the parent and use event bubbling to detect which child triggered the event.

It is useful for:
- Improving performance (fewer event listeners)
- Handling dynamic elements added after the event listener is set
- Reducing memory usage

In this project, we use event delegation in the main click handler to handle heart, copy, and call button clicks without attaching individual listeners to each button.

### 5. What is the difference between preventDefault() and stopPropagation() methods?

**preventDefault()**: Prevents the default action that belongs to the event. For example, preventing a link from navigating or a form from submitting. It stops the browser's default behavior.

**stopPropagation()**: Stops the event from bubbling up or capturing down the DOM tree, preventing other event listeners on ancestor elements from being triggered. It stops the event from propagating through the DOM.

In this project, we don't use these methods extensively since we're not dealing with forms or links that need default behavior prevention, but they are important concepts in JavaScript event handling.

## Contributing
Contributions are welcome. Please fork the repository and submit a pull request.

## License
This project is open source and available under the MIT License.
