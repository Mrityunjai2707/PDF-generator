# Tutorial: Generating Dynamic PDFs with React and Node.js

## Introduction

Welcome to this comprehensive guide on generating dynamic PDFs using React and Node.js. This tutorial is based on the informative article available on [Medium](https://medium.freecodecamp.org/how-to-generate-dynamic-pdfs-using-react-and-nodejs-eac9e9cb4dde). By following along, you'll gain practical insights into creating PDFs dynamically, leveraging HTML code as a template.

## Project Setup

Let's kickstart the project setup process:

1. **Create Directory:** Begin by creating a new directory named `pdfGenerator` using the following command:

    ```
    mkdir pdfGenerator && cd pdfGenerator
    ```

2. **Set Up React App:** Inside the newly created directory, initiate a React app named `client` with the command:

    ```
    create-react-app client
    ```

    Then, navigate into the newly created `client` directory and install the required dependencies:

    ```
    cd client && npm i -S axios file-saver
    ```

3. **Initialize Express Server:** Now, let's set up an Express server. Create a directory named `server`, navigate into it, and create a file named `index.js`. Initialize the `package.json` file by running:

    ```
    mkdir server && cd server && touch index.js && npm init
    ```

    Press enter a couple of times to initialize `package.json`, then install the necessary dependencies:

    ```
    npm i -S express body-parser cors html-pdf
    ```

4. **Configure Proxy:** To enable communication between the client and server, add a proxy configuration inside `client/package.json`. Above the dependencies, include the following line:

    ```
    "proxy": "http://localhost:5000/"
    ```

    This allows the client to make requests to the localhost server.

5. **Run the Application:** Open two separate terminals. In the first one, navigate to the `client` directory and start the React app:

    ```
    cd client
    npm start
    ```

    In the second terminal, navigate to the `server` directory and run the Express server using `nodemon`:

    ```
    cd server
    nodemon index.js
    ```

By following these steps, you'll have a robust setup for generating dynamic PDFs using React and Node.js.
