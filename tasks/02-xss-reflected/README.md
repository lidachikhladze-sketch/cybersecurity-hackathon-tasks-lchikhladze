# Task 2 – Reflected XSS (Google XSS Game – Level 1)

## Challenge

Find and exploit a reflected XSS vulnerability in the Google XSS Game (Level 1) and trigger an alert box with:
"Hackathon 2025"

Target URL:  
https://xss-game.appspot.com/level1

This is an intentionally vulnerable environment designed for practice.

---

## Approach

1. Open the Level 1 challenge.
2. Inspect how user input is reflected in the search box.
3. Inject a payload that breaks out of the HTML attribute context.
4. Insert a `<script>` tag that executes JavaScript in the victim's browser.

### ✔️ Working XSS Payload

```html
"><script>alert('Hackathon 2025')</script>

Target URL:  
https://xss-game.appspot.com/level1

This is an intentionally vulnerable environment designed for practice.

---

## Approach

1. Open the Level 1 challenge.
2. Inspect how user input is reflected in the search box.
3. Inject a payload that breaks out of the HTML attribute context.
4. Insert a `<script>` tag that executes JavaScript in the victim's browser.

### ✔️ Working XSS Payload

```html
"><script>alert('Hackathon 2025')</script>
