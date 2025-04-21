# PersonaQuest

This Flask-based application generates personality quizzes based on different themes using the Gemini API. It presents users with a series of questions and, upon submission, determines the character they most closely resemble within the selected theme.

## Features

-   **Theme Selection:** Users can choose from a variety of themes such as anime characters, fruits, colors, Harry Potter characters, mythical creatures, and desserts.
-   **Dynamic Quiz Generation:** The application dynamically generates quiz questions and options using the Gemini API based on the selected theme.
-   **Character Matching:** After the user submits their answers, the application uses the Gemini API to determine the best-matching character from the selected theme.
-   **Result Display:** The application displays the character the user matches, along with a personality description, strengths, and a relevant quote.

## Prerequisites

Before running the application, ensure you have the following:

-   Python 3.6 or higher
-   Flask
-   Sentence Transformers
-   dotenv
-   Google Generative AI API (Gemini)

You will also need a Google Generative AI API key.

## Installation

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd Personality-Quiz
    ```

2.  Create a virtual environment (recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```

3.  Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4.  Set up your Google Generative AI API key:

    -   Create a `.env` file in the project directory.
    -   Add your API key to the `.env` file:

        ```
        API_KEY=YOUR_API_KEY
        ```

## Usage

1.  Run the Flask application:

    ```bash
    python app.py
    ```

2.  Open your web browser and go to `http://127.0.0.1:5000` to access the application.

3.  Select a theme from the home page.

4.  Answer the quiz questions.

5.  Submit the quiz to see your result.

## Project Structure

-   `app.py`: Contains the Flask application logic, including route handling, API calls, and result processing.
-   `templates/`: Contains the HTML templates for rendering the quiz and result pages.
    -   `theme-select.html`: Template for selecting the quiz theme.
    -   `quiz.html`: Template for displaying the quiz questions and options.
    -   `result.html`: Template for displaying the quiz results.
-   `static/`: Contains static files such as CSS stylesheets and images (if any).
-   `.env`: Stores the API key (should not be committed to version control).
-   `README.md`: Provides an overview of the project and instructions for running it.
-   `requirements.txt`: Lists the Python packages required to run the application.

## Dependencies

-   Flask: A web framework for Python.
-   Sentence Transformers: A library for generating sentence embeddings.
-   python-dotenv: A library for loading environment variables from a `.env` file.
-   Google Generative AI API: Used for generating quiz questions and determining character matches.

## Error Handling

The application includes basic error handling for invalid theme selections and API-related issues. If an error occurs during the Gemini API call or result parsing, a generic error message is displayed.

## Future Enhancements

-   Implement a more sophisticated character matching algorithm using sentence embeddings.
-   Add user authentication and store quiz results in a database.
-   Expand the range of themes and characters.
-   Improve the user interface with more styling and interactivity.
-   Implement more robust error handling and logging.

## License

[Choose a license, e.g., MIT License]
