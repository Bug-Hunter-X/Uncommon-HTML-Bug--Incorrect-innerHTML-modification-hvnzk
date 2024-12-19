# Uncommon HTML Bug: Incorrect innerHTML Modification

This repository demonstrates a subtle bug in HTML involving the incorrect use of `innerHTML` to modify an element's content before the element is fully loaded into the DOM.  The script attempts to modify `myDiv` before the browser has finished parsing the HTML structure, resulting in an error.

## Bug Description
The bug lies in the script attempting to modify the `innerHTML` of the element with id `myDiv` before the browser has finished rendering the HTML page.  This leads to a runtime error because `document.getElementById('myDiv')` will return `null` before the element is created.

## Solution
The solution involves ensuring the script runs after the DOM is fully loaded using the `DOMContentLoaded` event listener.  This guarantees that the element exists before attempting to modify its content.