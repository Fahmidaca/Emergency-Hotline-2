# Emergency Hotline Project - README

## Questions and Answers

### 1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

- **getElementById**: Returns a single element object that has the specified ID. It is fast and unique since IDs should be unique in the DOM.
- **getElementsByClassName**: Returns a live HTMLCollection of all elements that have the specified class name. It updates automatically if the DOM changes.
- **querySelector**: Returns the first element that matches a specified CSS selector string. It is versatile and can select by ID, class, tag, attribute, etc.
- **querySelectorAll**: Returns a static NodeList of all elements matching the specified CSS selector string. Unlike getElementsByClassName, it does not update automatically.

### 2. How do you create and insert a new element into the DOM?

- You create a new element using `document.createElement(tagName)`.
- You can set attributes, classes, or content on the new element.
- To insert it into the DOM, use methods like `appendChild()`, `insertBefore()`, or `replaceChild()` on a parent node.
- Example:
  ```js
  const newDiv = document.createElement('div');
  newDiv.textContent = 'Hello World';
  document.body.appendChild(newDiv);
  ```

### 3. What is Event Bubbling and how does it work?

- Event Bubbling is a type of event propagation where an event starts from the deepest target element and then bubbles up to its ancestors in the DOM tree.
- For example, if you click a button inside a div, the click event triggers on the button first, then on the div, then on its parent elements up to the document.
- This allows event handlers on parent elements to catch events from their children.

### 4. What is Event Delegation in JavaScript? Why is it useful?

- Event Delegation is a technique where a single event listener is added to a parent element to handle events for its child elements.
- Instead of attaching event listeners to multiple child elements, you listen on the parent and use event bubbling to detect which child triggered the event.
- It is useful for improving performance and handling dynamic elements added after the event listener is set.

### 5. What is the difference between preventDefault() and stopPropagation() methods?

- **preventDefault()**: Prevents the default action that belongs to the event. For example, preventing a link from navigating or a form from submitting.
- **stopPropagation()**: Stops the event from bubbling up or capturing down the DOM tree, preventing other event listeners on ancestor elements from being triggered.
