# Multi-Profile Browser Automation Script

A Python script designed to automate repetitive daily web searches across multiple Microsoft Edge browser profiles. This tool leverages GUI automation to programmatically launch, arrange, and interact with browser windows to streamline repetitive tasks.

## Overview

This project was born out of a need to automate a personal, time-consuming daily task. The script opens batches of four Microsoft Edge profiles, arranges them on the screen, performs a series of generated search queries in each, and then closes them, repeating the process until all specified profiles have been used. It serves as a practical example of using Python for desktop automation and efficiency.

## Features

-   **Multi-Profile Management:** Launches specified Microsoft Edge profiles in sequential batches.
-   **Automated Window Arrangement:** Automatically arranges the four browser windows on the screen for easy monitoring.
-   **Algorithmic Search Generation:** Uses `itertools` to create a list of unique search term permutations for automated queries.
-   **GUI Automation:** Leverages `pyautogui` to simulate user actions like clicking on search bars, typing text, and pressing Enter.
-   **Batch Processing:** Processes all specified profiles in an automated workflow from start to finish.

## Technologies Used

-   **Language:** Python 3
-   **Libraries:**
    -   `pyautogui`: For controlling the mouse and keyboard to perform GUI automation.
    -   `subprocess`: For launching the Microsoft Edge application processes.
    -   `itertools`: For generating search query permutations.
    -   `time`, `random`: For managing delays and adding slight variations.

## Prerequisites

-   Python 3.x installed on your system.
-   Microsoft Edge Browser installed in the default location.

## Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/22A31A0525/Automated-Browser-Tasks.git](
    cd your-repository-name
    ```

2.  **Install the required library:**
    ```bash
    pip install pyautogui
    ```

## Configuration

**IMPORTANT:** This script relies on **hardcoded screen coordinates** for all mouse clicks (e.g., closing a window, clicking a search bar). These coordinates are specific to the developer's screen resolution (likely 1920x1080) and window layout.

For the script to work on your machine, you **must** find and replace the coordinate values in the following lists with your own:
-   `close_chrm`
-   `indication`
-   `search_bar`
-   `arrange_lst`

You can find your screen coordinates by running a simple Python script with `pyautogui.displayMousePosition()` or using other screen coordinate tools.

Additionally, you need to customize the `user_lst` with the directory names of your own Microsoft Edge profiles.

## Usage

1.  **Configure:** Open the `Automated_Browser_Interaction_Using_Python.py` file and update the coordinate lists and the `user_lst` as described in the Configuration section.
2.  **Run:** Execute the script from your terminal.
    ```bash
    python Automated_Browser_Interaction_Using_Python.py
    ```
    Ensure you do not move the mouse or use the keyboard while the script is running.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
