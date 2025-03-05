# codegen - AI-Powered Code Generator

[![Website](https://img.shields.io/badge/Website-hwkims.github.io%2Fcodegen-blue.svg)](https://hwkims.github.io/codegen/)

`codegen` is a web-based tool that leverages the power of AI to generate and debug HTML, CSS, and JavaScript code.  It provides a user-friendly interface to interact with different AI models, including OpenAI, Gemini, and Mistral, to create web components and applications.

## Features

*   **Multi-AI Model Support:** Choose between OpenAI, Gemini, and Mistral AI models to generate your code.  Easily switch between models and compare results.
*   **Interactive Chat Interface:**  Provide instructions in natural language, and the AI will generate the corresponding code.
*   **Real-time Code Editing:**  A built-in code editor (powered by CodeMirror) with syntax highlighting, auto-completion (tags and brackets), and line numbers.
*   **Live Preview:**  Instantly see the output of your generated code in an embedded iframe.  The preview updates as you type in the code editor.
*   **Automatic Error Handling:**  `codegen` attempts to automatically debug and fix errors reported by the browser's JavaScript console.  If an error occurs, the AI will try to generate corrected code (up to 3 attempts).
*   **API Key Management:**  Securely store your API keys for each AI model locally using `localStorage`.  Keys are automatically loaded when you switch between models.
*   **Responsive Design:** The layout adapts to different screen sizes, making it usable on desktops, tablets, and mobile devices.
*   **Modern UI:** A clean, modern design with a dark theme, using CSS gradients and shadows for a visually appealing experience.

## How to Use

1.  **Set API Keys:**
    *   Select your desired AI model from the dropdown (OpenAI, Gemini, Mistral).
    *   Enter your API key for the selected model in the input field.
    *   Click "Save API Key".  The key will be stored in your browser's local storage.

2.  **Interact with the AI:**
    *   Type your code request (e.g., "Create a responsive navigation bar with a logo and three links") in the input field at the bottom of the chat area.
    *   Press Enter or click the "Generate" button.

3.  **View and Edit Code:**
    *   The generated code will appear in the chat window and automatically populate the code editor.
    *   The code editor is a full-featured instance of CodeMirror, allowing you to edit the generated code directly.
    *   Changes made in the code editor are immediately reflected in the live preview.

4.  **See Live Preview:**
    *   The generated HTML, CSS, and JavaScript are rendered in real-time within the iframe.

5.  **Error Handling:**
    *   If the generated code has errors, they will be displayed in the chat.
    *   The system will automatically attempt to debug and fix the code by sending the error message and the code back to the AI.
    *   If the AI cannot fix the error after three attempts, a message will be displayed.

## Technologies Used

*   **HTML:**  The structure of the web page.
*   **CSS:**  Styling and layout (including responsive design using media queries).
*   **JavaScript:**  Interactivity, AI communication, and code editor integration.
*   **CodeMirror:**  A versatile text editor implemented in JavaScript for the browser.  Used for code editing with syntax highlighting, auto-completion, and more.  ( [https://codemirror.net/](https://codemirror.net/) )
*   **AI Models:**
    *   **OpenAI:**  Uses the `gpt-3.5-turbo` model for code generation.
    *   **Gemini:**  Uses the `gemini-pro` model for code generation.
    *   **Mistral:** Uses the `mistral-large` model (note: the provided code includes a placeholder URL for the Mistral API,  `https://api.mixtral.ai/v1/chat/completions`, which may need to be updated with the correct endpoint).
*   **Fetch API:**  Used for making asynchronous HTTP requests to the AI model APIs.
*   **localStorage:** Used for persisting API keys in the user's browser.

## Supported Browsers
Modern browsers that support the Fetch API, `async/await`, and `localStorage` such as Chrome, Firefox, Safari, and Edge.

## Development

To run this project locally:

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  Open `index.html` in your web browser.

## Contributing

Contributions are welcome!  Please feel free to submit pull requests or open issues for bug fixes, feature suggestions, or improvements.

## License

This project is open-source and available under the [MIT License](LICENSE) (You'll need to create a LICENSE file and add the MIT license text).

## Notes and Potential Improvements

*   **Mistral API Endpoint:**  The Mistral API endpoint (`https://api.mixtral.ai/v1/chat/completions`) is a placeholder.  You'll need to verify the correct endpoint for the `mistral-large` model.
*   **Error Handling:** The error handling could be made more robust by:
    *   Providing more context to the AI for error correction (e.g., including surrounding code).
    *   Implementing a more sophisticated error parsing mechanism.
    *   Allowing users to manually trigger error correction.
* **Token Limit:** Consider showing a message/warning if prompt+generated exceeds model token length.
* **Model Parameter Customization:** Consider adding UI to adjust the model parameters such as `max_tokens`, temperature, etc.
* **Code Formatting:** Consider adding a code formatter like Prettier.
*   **Session Management:** Implement a way to save and load previous chat sessions and generated code.
*   **Multiple Files:**  Support generating and editing multiple files (e.g., separate HTML, CSS, and JavaScript files).
* **UI library/framework Integration:** Add options to generate code that uses popular front-end libraries or frameworks like React, Vue, or Angular.

This improved README provides a comprehensive overview of the `codegen` project, including its features, usage instructions, underlying technologies, and potential future improvements.  It also includes clear instructions for setting up API keys and running the project locally. It also adheres to standard README best practices.
