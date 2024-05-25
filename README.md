# Messages of Hope - Website v1

> ### Important Notice
>
> This project is no longer in development. Due to significant design changes and improper use of git i.e. storing large blob files and libraries, it was not efficient to continue to use this project. Futhermore, this repository contains no official/easy way to deploy the website. This project was continued in a new repository with a new design and structure. The new repository can be found [here](https://git.jonathande.dev/messages-of-hope/website-v2).
>
> This repository is kept for historical purposes and to show the progression of the project.

The source code used to server the static Messages of Hope website. The project used NodeJS to serve static files for specific routes and to handle the contact form submission.

## Frontend

The frontend of the website was built using HTML, CSS, and JavaScript. The website was designed to be responsive and mobile-friendly, simple and easy to navigate. Each page is contained in a separate directory with the necessary files for that page. Shared resources are stored in the `shared` directory.

Each directory is marked with an underscore `_` to indicate that it is a directory and not a file. The directory structure is as follows:

- `index.html` - The main page of the website.
- `styles.css` - The CSS file for the page.
- `scripts.js` - The JavaScript file for the page.
- `assets` - The directory containing all the assets for the page.

## Backend

The backend of the website was built using NodeJS. The backend was used to serve the static files for the website and to handle the contact form submission. The backend is contained in the `moh-server.js` file. The backend uses the `express` library to handle the routing with the `express.static` middleware to serve the static files. The POST request for the contact form is handled by a separate file `contact-server.js`.

Any messages that are submitted through the website are stored in the `messages.csv` file. 

The contact form submission is handled by the `contact-server.js` file. The file reads the form data and adds it to the `contact-form.txt` file. We then use command line tools to send an email to the admin with the form data.
