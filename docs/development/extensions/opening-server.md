---
title: Opening an HTTP Server For Testing
---
# Setting Up an HTTP Server for Local Testing

## Requirements:
- Node.js installed on your system
- Basic knowledge of the command line

## Steps:

1. **Create a Project Directory:**
   - Open your terminal or command prompt.
   - Navigate to the directory where you want to create your project.

2. **Initialize a Node.js Project:**
   ```bash
   npm init -y
   ```

3. **Install the `http-server` Package:**
   ```bash
   npm install http-server --save-dev
   ```

4. **Create Your JavaScript Files:**
   - Create an `extension.js` file, this will be your extensions code.
    - *Example of what your extenion.js might look like:*
  ```javascript
(function(Scratch) {
  'use strict';
  class Extension {
    getInfo() {
      return {
        id: "johnMyExtension",
        name: "My Extension",
        blocks: [
          {
            opcode: 'logToConsole',
            text: 'log to console',
            blockType: Scratch.BlockType.COMMAND
          },
          {
            opcode: 'testReporter',
            text: 'testing!',
            blockType: Scratch.BlockType.REPORTER,
            disableMonitor: true,
	    allowDropAnywhere: true
          }
        ]
      };
    }

    logToConsole() {
      console.log('Hello world!');
    }
    testReporter() {
      return "Hello world!";
    }
  }

  Scratch.extensions.register(new Extension());
})(Scratch);
  ```

5. **Start the HTTP Server:**
   - In your terminal, navigate to your project directory.
   - Run the following command to start the server:
     ```bash
     npx http-server
     ```
   This command starts the server and serves files from the current directory.

6. **Access Your Local Server:**
   - Open a web browser.
   - Go to `http://localhost:8080/extension.js` or `http://127.0.0.1:8080/extension.js` in the address bar.
   - You should see your `extenion.js` file rendered in the browser.

7. **Testing:**
   - Make any changes to your JavaScript files.
   - Refresh the browser to see the changes instantly.
8. *Opening in Snail IDE:*
   - Load `http://localhost:8080/extension.js` or `http://127.0.0.1:8080/extension.js` in the custom extension menu,

9. **Stopping the Server:**
   - To stop the server, go back to the terminal where the server is running.
   - Press `Ctrl + C` to stop the server.

## Additional Notes:
- By default, the `http-server` package serves files on port `8080`.
- You can specify a different port using the `-p` or `--port` option followed by the desired port number when starting the server, like `npx http-server -p 3000`.
- Remember, this setup is intended for local testing only and should not be used for production purposes.
