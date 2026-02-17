# KodeKloud Downloader

A simple CLI tool to download courses and quizzes from KodeKloud.

## Features
- Download courses (videos and resources).
- Download quizzes as Markdown.
- Select specific video quality (360p - 1080p).
- Resume capability (skips existing files).

## Installation

1.  **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd KodeKloud-Downloader
    ```

2.  **Create a Virtual Environment**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Get Your Cookie**:
    - Log in to KodeKloud in your browser.
    - Use a browser extension (like "Get cookies.txt LOCALLY") to export your cookies in Netscape format.
    - Save the file as `cookie.txt` in the project root.

## Usage

Run the tool using the provided entry script:

### Download Courses
```bash
python run.py dl --cookie cookie.txt
```
To download a specific course by URL:
```bash
python run.py dl https://learn.kodekloud.com/courses/example-course --cookie cookie.txt
```

### Download Quizzes
```bash
python run.py dl-quiz --cookie cookie.txt
```

### Options
- `--quality <QUALITY>`: Set video quality (e.g., `720p`).
- `--output-dir <PATH>`: Set download directory.
- `--max-duplicate-count <INT>`: strict checking for duplicates.

## Disclaimer
This tool is for educational purposes only. Please respect KodeKloud's terms of service.
