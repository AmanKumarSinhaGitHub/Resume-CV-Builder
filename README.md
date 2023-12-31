# React Resume Builder App

## Overview
Welcome to the React Resume Builder App! This application simplifies the process of creating a professional resume by allowing users to input their personal and professional details. The application is structured with components such as `App`, `ResumeCreator`, and `Resume`, each handling specific functionalities.

## LIVE
[Open - React Resume Builder](https://amankumarsinhagithub.github.io/Resume-CV-Builder/)

## Fixes and To-Do
- **Fix Me:**
  - Enhance the Print Resume functionality.
  - Polish CSS styling for a more visually appealing experience.

- **To Do:**
  - Create a Home Page to improve navigation.
  - Implement a seamless flow: Home Page -> Resume Builder Form -> Generate Resume.

## Project Structure
- **`App.js`:**
  - The main component managing the overall structure of the application.
  - Utilizes state to manage user details.

```javascript
// ... (imports)

function App() {
  // ... (state and functions)

  return (
    <>
      <ResumeCreator getDetails={getUserDetails}/>
      <Resume {...details} />
    </>
  );
}

export default App;
```

- **`ResumeCreator.js`:**
  - Component responsible for capturing user input.
  - Handles details such as name, experience, education, skills, hobbies, and interests.

```javascript
// ... (imports)

function ResumeCreator({ getDetails }) {
  // ... (state and functions)

  return (
    <>
      {/* ... (input fields for various details) */}
      <button id="submitBtn" onClick={handleSubmit} className="btn">SUBMIT</button>
    </>
  );
}

export default ResumeCreator;
```

- **`Resume.js`:**
  - Component to display the generated resume based on user input.
  - Includes a dark/light theme toggle and print functionality.

```javascript
// ... (imports)

function Resume({ name, experience, education, skills, hobbies, interests }) {
  // ... (state and functions)

  return (
    <>
      <div className={`${isDarkMode ? "dark-theme" : "light-theme"}`}>
        {/* ... (resume content) */}
      </div>
    </>
  );
}

export default Resume;
```

## CSS
- The CSS files (`App.css`, `ResumeCreator.css`, `Resume.css`) require attention for better styling.
- Ensure a consistent and visually appealing design.

## How to Run
1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the application with `npm run dev`.

## Contributing
If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with descriptive messages.
4. Push your changes to your fork.
5. Submit a pull request.

Feel free to improve and enhance the React Resume Builder App. Your contributions are greatly appreciated!