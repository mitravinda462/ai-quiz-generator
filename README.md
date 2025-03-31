# AI Quiz Generator for Kahoot

## Overview
This a Python script that automatically generates multiple-choice quiz questions, specifically for Kahoot platform, using the Google Gemini API. It formats the questions in a structured way, saves them to an Excel file, and stores any related code or equations as images for easy reference.

## Features
- **AI-generated Quiz Questions**: Uses Google's Gemini API to create multiple-choice questions.
- **Excel Output**: Saves the quiz questions in an Excel (.xlsx) file for easy upload to platforms like Kahoot.
- **Image Storage**: Converts additional code snippets or equations into images for better readability.
- **Batch Download**: Stores all generated images in a folder for easy download.

## Installation
Ensure you have Python 3.7+ installed, then install the required dependencies:

```sh
pip install google-generativeai pandas openpyxl langchain langchain_community langchain-google-genai
```

## Setup
1. Obtain an API key from Google Gemini and replace `YOUR_API_KEY_HERE` in the script.
2. Ensure you have the necessary Python libraries installed.

## Usage
Run the cells in ai_quiz_generotor.ipynb or

Run the script with:
```sh
python ai_quiz_generator.py
```

The script will:
- Generate quiz questions on a specified topic.
- Save them to `quiz.xlsx`.
- Store related code or equations as images inside the `quiz_images/` folder.

## File Structure
```
/ai_quiz_generator
│── ai_quiz_generator.py  # Main script
│── ai_quiz_generator.ipynd  # Notebook
│── quiz.xlsx             # Generated quiz questions (output)
│── quiz_images/          # Folder containing code/equation images
│── quiz_images.zip  # zip file of images folder
│── README.md             # Documentation
```

## Example Output
A sample Excel row:

| Question | Answer 1 | Answer 2 | Answer 3 | Answer 4 | Correct Answer | Time Limit |
|----------|----------|----------|----------|----------|---------------|------------|
| What is the output of the following Swift code? | 3 | 8 | 15 | Error | 3 | 30 |

An image (`quiz_images/extra_info_1.jpg`) will contain the code snippet:
```swift
func calculate(x: Int, y: Int = 5) -> Int { return x * y }
print(calculate(x: 3))
```

## Troubleshooting
- **Output Parsing Error?** Ensure the API returns valid JSON.
- **Font Issues in Images?** Modify the `ImageFont` settings in the script.


