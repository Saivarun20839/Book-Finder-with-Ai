
# 📚 Book Finder with AI

A React-based web application that allows users to search for books, view detailed information, and interact with an AI assistant powered by Vapi. The app fetches data from the Open Library API.

---

## 🧪 Technologies Used

- **Frontend**: React, JavaScript (ES6+), CSS
- **Voice Assistant**: Vapi AI
- **Book Data Source**: Open Library API

---

---

## 🧩 Detailed Code Explanation

### `App.js`

- **Purpose**: Main component that handles state management, book search, voice assistant, and modal display.
- **State Variables**:
  - `query`: Current search query from user input.
  - `books`: List of books fetched from Open Library.
  - `loading`: Loading state for API requests.
  - `isListening`: Tracks if the voice assistant is listening.
  - `isSpeaking`: Tracks if the assistant is speaking.
  - `liveText`: Stores live transcription from voice input.
  - `assistantReply`: Stores AI assistant response.
  - `selectedBook`: Stores book details for modal view.
  - `message`: General messages displayed to the user.
- **Functions**:
  - `handleInputChange`: Updates query state as user types.
  - `handleSearch`: Fetches books from Open Library API based on `query`.
  - `toggleVoiceAssistant`: Starts/stops voice assistant using Vapi SDK.
  - `handleBookClick`: Fetches detailed info about a book and opens modal.
- **Effects**:
  - Listens for `speech` and `transcript` events from Vapi.
  - Disables scroll when modal is open.
- **JSX**:
  - Renders `Navbar`, `SearchBar`, `AiAssistant`, `BookList`, `BookModal`, and message box.

---

### `AiAssistant.js`

- **Purpose**: Renders AI assistant avatar and status.
- **Props**:
  - `isListening`, `isSpeaking`, `liveText`, `assistantReply`
- **Features**:
  - Shows AI avatar and pulse animation when speaking.
  - Displays assistant status: "Listening", "Speaking", "Waiting".
  - Displays live transcription (`liveText`) and assistant response (`assistantReply`).

---

### `BookList.js`

- **Purpose**: Display a list of books fetched from Open Library.
- **Props**:
  - `books`: Array of book objects.
  - `onBookClick`: Callback for handling click on a book.
- **Features**:
  - Maps `books` and shows title, author, cover.
  - Click triggers `onBookClick` to fetch book details.

---

### `BookModal.js`

- **Purpose**: Shows detailed info about a selected book.
- **Props**:
  - `selectedBook`: Book object with detailed info.
  - `onClose`: Callback to close the modal.
- **Features**:
  - Displays title, author, publication date, description.
  - Close button triggers `onClose`.

---

### `Navbar.js`

- **Purpose**: Navigation bar at the top.
- **Features**:
  - Can include links to sections or external resources.
  - Styled using CSS.

---

### `SearchBar.js`

- **Purpose**: Allows user to search for books.
- **Props**:
  - `query`: Search input value.
  - `onInputChange`: Updates query state.
  - `onSearch`: Triggers book search.
  - `toggleVoiceAssistant`: Activates voice input.
  - `isListening`: Indicates if voice assistant is active.
  - `loading`: Indicates API request loading state.
- **Features**:
  - Includes input box and search button.
  - Voice assistant button triggers `toggleVoiceAssistant`.

---

### `App.css`

- **Purpose**: Styles the layout, components, and animations.
- **Features**:
  - Layout styling for `main-container`, `BookList`, `BookModal`.
  - Spinner animation for loading state.
  - `animate-pulse` effect for AI assistant speaking.
  - Styling for messages, buttons, input fields, and modals.

---


# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)




