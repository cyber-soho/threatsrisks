Project: Self-Contained Course Outline Webpage

Overview

This repository contains the source code for interactive, and secure webpage for the "Threats & Risks" (420-1C2-DW) course outline for the Fall 2025 term fora large Public College.

The primary goal of this project is to deliver all course information in a single, portable HTML file that can be viewed offline, requires no external dependencies, and includes built-in security features like a strict Content Security Policy (CSP) and password protection.

Features :

Single-File Application: All HTML, CSS, and JavaScript are contained within index.html.

Password Protection:
The content is locked behind a password modal.

Password:
Contact  info.6gc0a@slmail.me

The password check is handled by client-side JavaScript, using btoa() (Base64 encoding) for simple obfuscation.

Interactive UI:

Dark/Light Mode: A theme toggle to switch between dark and light modes, with the user's preference saved in localStorage.

Search/Filter: A live search bar to filter the 10-week schedule by keywords.

Accordion Sections: Each week is a collapsible "accordion" section.

Expand/Collapse All: Buttons to open or close all weekly sections at once.

Print Functionality: A "Print" button that formats the page for printing or saving as a PDF (hiding interactive elements).

Responsive Design: The layout adapts to different screen sizes, from mobile to desktop.

Zero Dependencies: The file runs entirely on its own, with no external fonts, scripts, or stylesheets.

Security Features

A key aspect of this project is its hardened security model, enforced directly in the HTML:

Strict Content Security Policy (CSP): A strong CSP is implemented via a <meta> tag to prevent common web vulnerabilities.

default-src 'self': Restricts all resources to be loaded only from the file's own origin.

script-src 'self' 'nonce-...': Only allows scripts with a specific nonce to run, preventing inline scripts and XSS.

style-src 'self' 'nonce-...': Same as above, but for CSS.

All other sources (like connect-src, media-src, object-src) are set to 'none'.

Project Structure

While index.html is the main file, it contains relative links to other local HTML files, such as:

threats-and-risks.html

glpi_lab.html

freeipa_lab.html

ossec.html

maltego.html

...and many others for each class and lab.

To be fully functional, this index.html file expects all the linked .html files to be present in the same directory.

Technology Stack

HTML5

CSS3: Custom properties (variables) for theming, Flexbox, and Grid.

Vanilla JavaScript (ES6+): No frameworks or libraries are used. All functionality is custom-written.

How to Use

Clone the repository or download all files.

Ensure all .html files (like glpi_lab.html, ossec.html, etc.) are in the same folder as index.html.

Open index.html in any modern web browser.

When prompted, enter the password:  ask  info.6gc0a@slmail.me
