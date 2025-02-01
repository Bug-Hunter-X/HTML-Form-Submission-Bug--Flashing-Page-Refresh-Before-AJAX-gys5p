# HTML Form Submission Bug: Flashing Page Refresh Before AJAX

This repository demonstrates an uncommon bug related to HTML form submissions and AJAX.  Even with `event.preventDefault()` to stop default form submission, a brief page refresh might still occur before the AJAX call completes. This is due to how browsers handle form submissions.

## Bug Description
The issue occurs when using JavaScript to submit a form asynchronously with AJAX. Despite using `event.preventDefault()` to prevent the default form submission, a quick refresh of the page is visible before the AJAX request finishes.

## Bug Reproduction
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe the page refresh before the AJAX success message is displayed. 

## Solution
The solution involves carefully handling the form submission process to avoid conflicting behavior between the default submission and the AJAX handling. See `solution.html` for a corrected implementation.

## Technologies Used
- HTML
- JavaScript
- AJAX