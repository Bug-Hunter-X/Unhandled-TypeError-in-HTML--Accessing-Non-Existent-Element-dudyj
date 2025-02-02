# Unhandled TypeError in HTML: Accessing Non-Existent Element

This repository demonstrates an uncommon error in HTML that arises from attempting to access the properties of an element that may not exist in the DOM yet.  The error typically manifests as a `TypeError: Cannot read properties of undefined (reading 'innerHTML')` in the browser's console.

## Bug Description
The bug is caused by directly accessing the properties of an element that doesn't exist before the script attempting to access it has been loaded. This is a common mistake when trying to dynamically add content using JavaScript.

## Solution
The solution involves ensuring that the element exists before accessing its properties.  This can be achieved using various methods, such as:

* **Checking for the existence of the element:** Before accessing its properties. Use `document.getElementById()` and check if the returned value is not null.
* **Using optional chaining(?:):**  A more modern approach that allows accessing properties safely even if an intermediate object is null or undefined.  This is supported by modern browsers.
* **Event listeners:** Attaching event listeners such as DOMContentLoaded or load to execute your code after the page has loaded and the necessary elements are present. 

This repository includes both the buggy and the corrected code for demonstration purposes.