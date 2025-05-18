# llm2files

`llm2files` is an online tool to parse and extract files from Large Language Model (LLM) chat outputs (e.g., ChatGPT, Claude). It converts text containing specific delimiters into an organized file and folder structure, which can then be downloaded as a ZIP archive.

**Access the tool:** [https://llm2files.liniewicz.info/](https://llm2files.liniewicz.info/)

## Key Features

*   Parses text containing multiple files defined by delimiters like `-----filename.ext-----`.
*   Supports nested folder structures based on paths in delimiters (e.g., `-----folder/subfolder/file.ext-----`).
*   Provides a visual tree of the extracted files and folders.
*   Allows previewing the content of individual files.
*   Enables downloading the entire structure as a single `.zip\` file.
*   Operates entirely client-side: all data is processed in your browser for privacy.

## Usage

1. **Format LLM Output:** Instruct your LLM to output multiple files within a single response or code block\. You can use a prompt similar to the following:

    > IMPORTANT: If you choose to structure the output as multiple files, please output the code of all files in a SINGLE code block, inserting the names of files above their code as `-----filename.ext-----` or `-----somefolder/filename.ext-----`, `-----somefolder/anotherfolder/filename.ext-----`, and so on. Thank you very much.

    Each file should be preceded by a delimiter on its own line, indicating its path and name.
    *   Example delimiter: `-----path/to/your/filename.ext-----`
    *   The content of the file should follow immediately after its delimiter line.

    Example LLM Output:
    ```
    -----index.html-----
    <!DOCTYPE html>
    <html>
    <head>
        <title>My Page</title>
    </head>
    <body>
        <h1>Hello, World!</h1>
    </body>
    </html>
    -----css/style.css-----
    body {
        font-family: Arial, sans-serif;
    }
    h1 {
        color: navy;
    }
    ```

2.  **Input Data:**
    * Navigate to [llm2files](https://llm2files.liniewicz.info/).
    * Paste the LLM's response directly into the text area.
    * Alternatively, save the response as a `.txt` file and upload it using the "Choose File" button.

3.  **Process & Preview:**
    * Click the "Process Input" button.
    * The tool will display a file tree on the left. Click on any file in the tree to preview its content in the right-hand panel.

4.  **Download:**
    * Optionally, you can set a custom name for the root folder of your project before downloading.
    * Click the "Download ZIP" button to save all extracted files and folders as a `.zip` archive to your computer.

## Privacy

All processing is done locally in your web browser. No data is sent to or stored on any server.
