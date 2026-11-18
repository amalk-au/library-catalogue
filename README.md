# Library Catalogue

A lightweight library catalogue application (front end only) built with vanilla JavaScript, HTML and CSS, allowing users to add books, manage their reading status and maintain a dynamic list of books.

## Table of Contents

- [Overview](#overview)

- [Features](#features)

- [Screenshots](#screenshots)

- [Live Demo](#live-demo)

- [Tech Stack](#tech-stack)

- [Architecture](#architecture)

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)

  - [Installation](#installation)

- [Project Structure](#project-structure)

- [Available Commands](#available-commands)

- [Development](#development)

- [Testing](#testing)

- [Deployment](#deployment)

- [Troubleshooting](#troubleshooting)

- [Contributing](#contributing)

- [License](#license)

- [Acknowledgements](#acknowledgements)

- [Contact](#contact)

---

## Overview

Library Catalogue is a simple browser-based application developed using fundamental web technologies: HTML, CSS and JavaScript.

The application provides an interactive interface for maintaining a personal collection of books. Users can add book information, view their catalogue, update reading statuses and remove books from the collection.

The project demonstrates JavaScript fundamentals, including object-oriented programming, ES6 classes, DOM manipulation, event handling, arrays, browser form validation and dynamically generated HTML elements.

The application was originally developed as part of the JavaScript curriculum from [The Odin Project](https://www.theodinproject.com/).

## Features

- **Add Books:** Add new books by providing the author's name, book title and number of pages.

- **Book Catalogue:** Display dynamically generated book cards containing the information entered by the user.

- **Reading Status:** Record whether a book has been read and toggle its reading status.

- **Delete Books:** Remove individual books from the catalogue.

- **Form Validation:** Validate required fields and enforce input length and page-count restrictions.

- **Dynamic Interface:** Update the catalogue dynamically using JavaScript DOM manipulation without refreshing the page.

- **Object-Oriented JavaScript:** Represent individual books using JavaScript classes.

### Input Validation

The application implements the following input restrictions:

| Field           | Validation                             |
| --------------- | -------------------------------------- |
| Author Name     | Required, maximum 100 characters       |
| Book Title      | Required, maximum 100 characters       |
| Number of Pages | Required, minimum 10 and maximum 1,000 |
| Reading Status  | Radio button selection                 |

**Note:** Book information is maintained in an in-memory JavaScript array. Data is not persisted between browser sessions or page refreshes.

## Screenshots

Screenshots can be added to the `docs/screenshots/` directory.

### Application Overview

### Book Catalogue

### Add New Book

### Mobile View

## Live Demo

Explore the deployed application:

[**Library Catalogue – Live Demo**](https://amalk.au/library-catalogue/)

Source Code: [GitHub Repository](https://github.com/amalk-au/library-catalogue)

Portfolio: [https://amalk.au](https://amalk.au)

## Tech Stack

| Category                | Technology                                |
| ----------------------- | ----------------------------------------- |
| Frontend                | HTML5, CSS3                               |
| Programming Language    | JavaScript (ES6+)                         |
| Styling                 | CSS3                                      |
| JavaScript Architecture | Object-Oriented Programming (ES6 Classes) |
| DOM Manipulation        | JavaScript DOM APIs                       |
| Form Validation         | Native HTML5 Validation and JavaScript    |
| External Resources      | Google Fonts                              |
| Font Family             | Fredericka the Great                      |
| Package Manager         | Not Required                              |
| Backend                 | None                                      |
| Database                | None                                      |
| Hosting                 | Portfolio Domain                          |

## Architecture

Library Catalogue is a client-side application built using a simple separation of concerns.

The application consists of three primary components:

### 1\. HTML – Application Structure

`index.html` defines the application's structure, including:

- Main application heading.

- Library catalogue display area.

- Book submission form.

- Author, title and page-count input fields.

- Reading status radio buttons.

- Submission button.

The HTML document loads the stylesheet and JavaScript file directly.

### 2\. CSS – Presentation Layer

`styles.css` controls the application's visual presentation.

It defines:

- Typography and colours.

- Library catalogue layout.

- Book card styling.

- Form layout.

- Input validation feedback styling.

The application also uses the Fredericka the Great font through Google Fonts.

### 3\. JavaScript – Application Logic

`logic.js` implements the application's functionality using ES6 classes.

The main components include:

| Component          | Responsibility                                                               |
| ------------------ | ---------------------------------------------------------------------------- |
| `bookData`         | Represents an individual book and manages its reading status.                |
| `addBookToLibrary` | Collects form data, creates book objects and adds them to the library array. |
| `bookInfoDisplay`  | Dynamically generates and displays book information cards.                   |
| `formValidation`   | Validates user input and controls the submission button.                     |

### Application Data Flow

1.  The user enters book information through the HTML form.

2.  JavaScript validates the form inputs.

3.  Once the required fields are valid, the submission button becomes available.

4.  Submitting the form creates a new `bookData` object.

5.  The new book object is added to the `myLibrary` array.

6.  The catalogue is dynamically updated using DOM manipulation.

7.  Users can subsequently toggle reading status or delete individual books.

**Data Storage:** The `myLibrary` array is maintained in browser memory. No external database or persistent storage is currently implemented.

## Getting Started

### Prerequisites

The application has minimal development requirements.

- A modern web browser.

- Git (optional, for cloning the repository).

- A code editor (recommended: Visual Studio Code).

No Node.js installation, package manager, database or external backend service is required.

### Installation

1.  Clone the repository:

    ```
    git clone https://github.com/amalk-au/library-catalogue.git
    ```

2.  Navigate into the project directory:

    ```
    cd library-catalogue
    ```

3.  Open `index.html` in your preferred web browser.

    Alternatively, open the project directory in Visual Studio Code and use your preferred local static file server.

No dependency installation or environment configuration is required.

## Project Structure

```
library-catalogue/
│
├── docs/
│   └── screenshots/
│       ├── library-catalogue-desktop.png
│       ├── library-catalogue-books.png
│       ├── library-catalogue-add-book.png
│       └── library-catalogue-mobile.png
│
├── index.html          # Application HTML structure
├── logic.js            # Application logic and DOM manipulation
├── styles.css          # Application styling
├── LICENSE             # GNU General Public License v3.0
└── README.md           # Project documentation
```

The `docs/screenshots/` directory and its image files are suggested additions for project documentation. They are not included in the current repository.

## Available Commands

This project does not currently use a Node.js package configuration or build system.

| Command        | Description                                          |
| -------------- | ---------------------------------------------------- |
| Not Applicable | No package scripts or build commands are configured. |

There is no `package.json` or `pnpm-lock.yaml`.

The application can be developed and run directly in a web browser without installing project dependencies.

**Package Manager:** pnpm is not required for this project.

## Development

The project follows a straightforward development workflow using standard web technologies.

### Development Guidelines

1.  Clone the repository.

2.  Create a feature branch for your changes.

3.  Modify the relevant HTML, CSS or JavaScript files.

4.  Test the application in a modern web browser.

5.  Verify existing functionality after making changes.

6.  Commit your changes with meaningful commit messages.

7.  Submit a pull request if contributing to the repository.

### Development Considerations

- Keep HTML responsible for application structure.

- Use CSS for presentation and layout.

- Keep application logic within `logic.js`.

- Follow existing JavaScript naming and coding conventions.

- Prefer reusable functions and classes where appropriate.

- Validate user input before processing submitted data.

- Avoid introducing unnecessary dependencies.

## Testing

There is currently no automated testing framework or test suite configured in the repository.

Application functionality should be verified manually using a modern web browser.

### Recommended Manual Tests

| Test Case                    | Expected Behaviour                                |
| ---------------------------- | ------------------------------------------------- |
| Add a valid book             | A new book card appears in the catalogue.         |
| Submit an empty author field | The form prevents submission.                     |
| Submit an empty title field  | The form prevents submission.                     |
| Enter fewer than 10 pages    | The page-count validation reports an error.       |
| Enter more than 1,000 pages  | The page-count validation reports an error.       |
| Enter a valid page count     | The page-count validation accepts the input.      |
| Toggle reading status        | The selected book's reading status updates.       |
| Delete a book                | The selected book is removed from the catalogue.  |
| Delete all books             | The empty-library message is displayed.           |
| Refresh the browser          | Previously entered books are no longer available. |

## Deployment

The application is deployed under the following portfolio domain:

**Live URL:** [https://amalk.au/library-catalogue/](https://amalk.au/library-catalogue/)

**Portfolio:** [https://amalk.au](https://amalk.au)

### Deployment Requirements

This is a static frontend application and does not require:

- A backend server.

- Database provisioning.

- Environment variables.

- Server-side configuration.

- A JavaScript build process.

The deployment environment must serve the HTML, CSS and JavaScript files correctly.

### Subdirectory Deployment

The application currently references its assets using relative paths:

```
<link rel="stylesheet" href="./styles.css" />
<script src="./logic.js"></script>
```

These relative paths allow the application to be deployed under a subdirectory, such as:

```
https://amalk.au/library-catalogue/
```

When modifying asset paths or introducing additional resources, ensure they remain compatible with the deployment location.

## Troubleshooting

| Issue                                        | Possible Solution                                                                    |
| -------------------------------------------- | ------------------------------------------------------------------------------------ |
| Application does not load                    | Verify that `index.html` exists and is accessible.                                   |
| Styling is missing                           | Check that `styles.css` is correctly referenced.                                     |
| JavaScript functionality is unavailable      | Check the browser console for errors and verify the `logic.js` reference.            |
| Submission button remains disabled           | Verify that all required form fields contain valid values.                           |
| Google Font does not load                    | Check internet connectivity and Google Fonts availability.                           |
| Book information disappears after refreshing | This is expected behaviour because the application currently uses in-memory storage. |
| Application assets fail under a subdirectory | Verify that relative asset paths are preserved.                                      |

## Contributing

Contributions, suggestions and improvements are welcome.

To contribute:

1.  Fork the repository.

2.  Create a feature branch.

3.  Implement your changes.

4.  Test the application in a browser.

5.  Commit your changes with meaningful commit messages.

6.  Open a pull request describing your changes.

For significant changes, consider opening an issue before implementing the proposed functionality.

## License

This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.

You are free to use, modify and distribute this software under the terms of the licence.

See [LICENSE](LICENSE) for the full licence text.

## Acknowledgements

- [The Odin Project](https://www.theodinproject.com/) – Web development curriculum and project learning resources.

- [Google Fonts](https://fonts.google.com/) – Fredericka the Great typeface.

## Contact

- **Author:** Amal K.

- **GitHub:** [@amalk-au](https://github.com/amalk-au)

- **Portfolio:** [https://amalk.au](https://amalk.au)

- **Issues:** [GitHub Issues](https://github.com/amalk-au/library-catalogue/issues)

---

Developed by [amalk-au](https://github.com/amalk-au)
