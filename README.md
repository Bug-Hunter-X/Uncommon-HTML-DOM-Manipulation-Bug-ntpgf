# Uncommon HTML DOM Manipulation Bug

This repository demonstrates an uncommon bug related to DOM manipulation in HTML and JavaScript.  The bug arises from attempting to access a child element of a parent element after the parent's content has been cleared.  This often leads to a runtime error or unexpected behavior.

## Bug Description

The provided HTML code includes a div element and a button.  A JavaScript function is triggered when the button is clicked. This function clears the content of the div using `innerHTML = ""`, which removes all child elements.  Subsequently, the code attempts to access and modify a child element that no longer exists, resulting in an error.

## Solution

The solution involves checking if the child element exists before attempting to access it.  This prevents the error by handling the case where the element might have been removed.