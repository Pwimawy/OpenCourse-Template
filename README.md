# Course Data Repository

This repository serves as a collection point for course-specific questions and answers, structured in an easy-to-use JSON format. Each JSON file represents a single course, containing its title, contributor information, and a list of questions and their corresponding answers.

The goal is to provide a standardized way to store and share educational content, making it easy to integrate into various applications (like quiz apps, study tools, etc.).

---

## 🚀 Getting Started: Obtaining the Files

You have two primary ways to get the `Course000data.json` file:

### Option 1: Clone the Repository (Recommended for Contributors)

This method is ideal if you plan to contribute your changes back to this GitHub repository via a Pull Request.

1.  **Open your terminal or command prompt.**
2.  **Run the following command.** 

    ```bash
    git clone https://github.com/Pwimawy/OpenCourse-Template.git
    ```

3.  **Navigate to the Repository Directory.** Change your current directory to the newly cloned repository:

    ```bash
    cd [repository-name] # e.g., cd course-data-repository
    ```

### Option 2: Download as a ZIP File (For Local Use / Non-Git Users)

If you're not planning to use Git or just want to quickly get the files for local use, you can download the entire repository as a ZIP archive.

1.  **Go to the GitHub repository page.**
2.  **Click the green "Code" button.**
3.  **Select "Download ZIP"** from the dropdown menu.
4.  **Extract the ZIP file** to your desired location on your computer.

    *   **Note:** If you download as a ZIP, you won't be able to `git push` your changes directly back to GitHub. You would need to manually upload your modified JSON file either through the GitHub web interface (if you have permission) or via an alternative submission method (like Discord, described below). Cloning is recommended if you intend to make continuous contributions.

---

## ✍️ How to Contribute: Filling Up `Course000data.json`

The file you'll be editing is named `Course000data.json`. Open this file in your favorite code editor (like VS Code, Sublime Text, Atom, Notepad++, etc.).

Here's a breakdown of the JSON structure and how to fill it out:

```json
{
  "id": "course-000",
  "title": "UGRD-IT62 Advanced Information Management",
  "contributor": {
    "name": "Peter",
    "degree": "Bachelor of Science in Computer Science",
    "avatar": "/contributorpfp/blankpfp.jpg",
    "links": {
      "facebook": "https://www.facebook.com/",
      "instagram": "https://www.instagram.com/",
      "github": "https://github.com/",
      "youtube": "https://www.youtube.com/"
    }
  },
  "questions": [
    {
      "id": 1,
      "question": "Question 1 goes here... ",
      "answer": "Answer 1 goes here... "
    }
    // ... more questions
  ]
}
```

### 1. Update the Course `title`

This is where you put the name of the course you are contributing.

*   Locate the `"title"` key.
*   Replace `"UGRD-IT62 Advanced Information Management"` with your desired course title.

**Example:**

```json
"title": "Your Desired Contributed Course Name Here",
```

### 2. Add Your `contributor` Information

Fill in your details so that proper credit can be given.

*   Locate the `"contributor"` object.
*   **`"name"`**: Replace `"Peter"` with your full name.
*   **`"degree"`**: Replace `"Bachelor of Science in Computer Science"` with your relevant degree or qualification.
*   **`"avatar"`**: This is a path to your profile picture.
    *   If you have an avatar image within the repository (e.g., in a `contributorpfp` folder), provide its path (e.g., `"/contributorpfp/your_name.jpg"`).
    *   If you don't have one or prefer not to use one, you can leave it as `"/contributorpfp/blankpfp.jpg"` or an empty string `""`.
*   **`"links"`**: Update your social media and professional links.
    *   Replace the placeholder URLs with your actual profile links.
    *   If you don't have a specific platform link, you can leave the string empty `""` or keep the placeholder if it's a general project link.

**Example:**

```json
"contributor": {
  "name": "Jane Doe",
  "degree": "Master of Arts in English Literature",
  "avatar": "/contributorpfp/jane_doe.jpg",
  "links": {
    "facebook": "https://www.facebook.com/janedoe",
    "instagram": "",
    "github": "https://github.com/janedoe",
    "youtube": ""
  }
},
```

### 3. Add Questions and Answers

This is the main content of the course file. The `questions` field is an array of objects, where each object represents one question and its answer.

*   Locate the `"questions"` array.
*   Each question is an object with three fields:
    *   **`"id"`**: A unique number for each question within this course file. **Ensure this ID is sequential and unique for every question.**
    *   **`"question"`**: The actual question text.
    *   **`"answer"`**: The corresponding answer text.

#### Filling Existing Question Placeholders:

For the existing placeholder questions (e.g., `id: 1` through `id: 100` in your example):

*   Replace `" "` (the empty string) in both `"question"` and `"answer"` with your actual content.

**Example:**

```json
{
  "id": 1,
  "question": "What is the capital of France?",
  "answer": "Paris"
},
```

#### Adding More Questions:

If you need more than the pre-defined number of questions:

1.  Copy an existing question object (from the `{ "id": ..., "question": ..., "answer": ... }` block).
2.  Paste it **after** the last question object in the array.
3.  **Important:** Make sure there's a comma `,` separating each question object, except for the very last one in the array.
4.  **Increment the `"id"`**: Update the `id` of the new question to be the next sequential number.
5.  Fill in the `"question"` and `"answer"` for your new entry.

**Example (adding a new question after `id: 1`):**

```json
{
  "id": 1,
  "question": "What is the capital of France?",
  "answer": "Paris"
},  // <--- Don't forget the comma here!
{
  "id": 2, // <--- Increment the ID!
  "question": "What is 2 + 2?",
  "answer": "4"
},
// If this is the last question, no comma after it.
```

#### Removing Questions:

To remove a question, simply delete its entire object ` { "id": ..., "question": ..., "answer": ... } ` from the `questions` array. Remember to adjust commas if you're removing an item from the middle of the list.

### JSON Formatting Tips:

*   **Commas Matter**: Ensure there's a comma `,` after every element in a list (like questions) or key-value pair, **except for the very last one** in its block/array.
*   **Quotes**: All keys (like `"title"`, `"name"`, `"question"`) and string values (like `"Your Course Title"`, `"Your Name"`) **must** be enclosed in double quotes `""`.
*   **Brackets**: `{}` denote objects, and `[]` denote arrays (lists). Make sure they are correctly matched.
*   **Use a Linter**: Many code editors have built-in JSON linters or plugins that can help you catch syntax errors.

---

## 📤 Submitting Your Contribution

Once you've finished filling out `Course000data.json`, you have two ways to submit your work:

### Option 1: Via GitHub (Recommended for Git Users)

If you cloned the repository using Git and are comfortable with the workflow:

1.  **Save Your File.** Save the `Course000data.json` file in your code editor.

2.  **Stage Your Changes.** In your terminal, tell Git to include your changes for the next commit:

    ```bash
    git add Course000data.json
    ```
    (Or `git add .` to stage all changes in the current directory, but it's often better to be specific.)

3.  **Commit Your Changes.** Record your changes with a descriptive message:

    ```bash
    git commit -m "feat: Added questions for [Your Course Name]"
    ```
    Replace `[Your Course Name]` with the actual title of the course you updated.

4.  **Push to GitHub.** Send your committed changes to the GitHub repository:

    ```bash
    git push origin main
    # or git push origin master, depending on your branch name
    ```

5.  **Create a Pull Request.** If you don't have direct push access to the `main` branch, you might need to create a Pull Request on GitHub. After pushing your changes to your fork or a feature branch, navigate to the GitHub repository page and follow the prompts to create a new pull request. This allows the repository maintainers to review and merge your contribution.

### Option 2: Upload to OpenCourse Discord Server (Alternative for Non-Git Users)

If you downloaded the ZIP file or prefer not to use Git, you can submit your completed `Course000data.json` file directly to our Discord server.

1.  **Save Your File.** Make sure your `Course000data.json` file is saved with all your changes.
2.  **Join the "OpenCourse" Discord Server.** (If you haven't already).
3.  **Navigate to a designated submission channel.** Look for a channel like `#json-submissions`, `#course-contributions`, or a general `#discussions` channel. If unsure, ask a moderator where to submit.
4.  **Upload the `Course000data.json` file.**
    *   Drag and drop the file into the Discord chat.
    *   Or click the `+` icon next to the chat box, select "Upload a File", and choose your `Course000data.json`.
5.  **Add a brief message.** In your message, clearly state that this is your contribution for `[Your Course Name]`, mention your contributor name, and perhaps briefly describe the content. This helps maintainers process your submission efficiently.

    **Example Discord Message:**
    > "Hello! Here is my contribution for the 'Introduction to Python Programming' course. My contributor name is Jane Doe. Thanks for reviewing!"

---

Thank you for contributing to this project! Your efforts help expand our shared knowledge base.
```
