# Accessible Collaborative Word Editor

This is a simple, accessible, collaborative word editor built with HTML, CSS, JavaScript, and Firebase. It allows users to create, edit, and share documents in real-time.

## Features

*   **Real-time Collaboration:** Multiple users can edit the same document simultaneously.
*   **Multiple View Modes:** Supports Plaintext, Markdown, and Code views.
*   **Syntax Highlighting:** Code view includes syntax highlighting for various languages.
*   **Accessibility:** Designed with accessibility in mind, including high-contrast focus states and ARIA attributes.
*   **Document Sharing:** Easily share documents by copying and pasting the Document ID.
*   **Firebase Integration:** Uses Firebase for real-time database and authentication.
*   **Tailwind CSS:** Styled using Tailwind CSS for a modern and responsive design.
*   **Hot Action Bar:** Provides quick actions for selected text.

## Technologies Used

*   HTML
*   CSS (Tailwind CSS)
*   JavaScript
*   Firebase (Realtime Database, Authentication)
*   Marked.js (Markdown rendering)
*   Highlight.js (Syntax highlighting)

## Setup Instructions

1.  **Firebase Project:**
    *   Create a new project in the Firebase Console: [https://console.firebase.google.com/](https://console.firebase.google.com/)
    *   Enable Authentication (Anonymous) in the Firebase Console.
    *   Create a Realtime Database in the Firebase Console.

2.  **Configuration:**

    *   You will need to set the `__app_id` and `__firebase_config` global variables.  These are used to configure the Firebase connection. These are intentionally left undefined in the provided HTML.  The easiest way to do this is to define them *before* the script tag that includes the main application logic.

    ```html
    <script>
        const __app_id = "your-firebase-app-id";
        const __firebase_config = JSON.stringify({
            apiKey: "your-firebase-api-key",
            authDomain: "your-firebase-auth-domain",
            projectId: "your-firebase-project-id",
            storageBucket: "your-firebase-storage-bucket",
            messagingSenderId: "your-firebase-messaging-sender-id",
            appId: "your-firebase-app-id"
        });
    </script>
    <script type="module">
        // Your application logic here (from the provided HTML)
    </script>
    ```

    *   Replace `"your-firebase-app-id"`, `"your-firebase-api-key"`, etc. with the appropriate values from your Firebase project settings.  Make sure `__firebase_config` is valid JSON.

3.  **Include Firebase SDKs:**

    The necessary Firebase SDKs are included via CDN in the provided HTML.

4.  **Open the HTML file:**

    Open the `index.html` file in your web browser.

## Usage

1.  **Create a new document:** Click the "New Document" button to create a new document. A unique Document ID will be generated.
2.  **Share a document:** Copy the Document ID and share it with others.
3.  **Join a document:** Paste the Document ID into the "Join an Existing Document" field and click the "Join" button.
4.  **Edit the document:** Start typing in the editor area. Changes are automatically saved and synchronized with other users.  Double-click the view area to enter edit mode. Press Escape to exit edit mode.
5.  **Switch view modes:** Use the buttons in the "View as" section to switch between Plaintext, Markdown, and Code views.
6.  **Code View Language:**  Select the appropriate language from the dropdown when in code view.
7.  **Action Bar:** Select text to show the action bar.

## Accessibility

*   The editor is designed with accessibility in mind.
*   High-contrast focus rings are provided for keyboard users.
*   ARIA attributes are used to provide semantic information to assistive technologies.
*   The editor is keyboard navigable.

## Collaboration

*   Multiple users can edit the same document simultaneously.
*   Changes are synchronized in real-time using Firebase.
*   Share documents easily using the unique Document ID.

## Notes

*   This is a basic implementation and can be extended with more features.
*   Error handling and UI feedback could be improved.
*   Consider adding user authentication and authorization for more secure collaboration.
*   The styling can be customized further using Tailwind CSS.
*   The "Action Bar" functionality can be extended with more actions.

## License

[MIT](LICENSE) (Replace with your chosen license if applicable).

