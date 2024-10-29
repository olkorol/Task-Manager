# Task Manager

A command-line task management tool built with Python to help you organize tasks across various categories. Tasks can be scheduled with specific durations and dates, and categorized for easy management.

## Features

- **Category-based task storage**: Store tasks in `inbox`, `notes`, `calendar`, `someday_maybe`, `backlog`, `projects`, `done`, and `Task delegated`.
- **Task prioritization by duration**: Specify estimated durations for tasks, which are automatically sorted within each category.
- **Calendar sorting by date**: Tasks in the `calendar` category are sorted by planned date for easy scheduling.
- **Task delegation**: Assign tasks to others with an option to specify the responsible person.
  
## Setup

1. **Clone the repository**:

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install dependencies**:

   - This project uses only Python’s standard libraries, so no external dependencies are required.

3. **Add `tasks.json` to `.gitignore`**:

    To prevent Git from tracking `tasks.json`, add it to `.gitignore`:

    ```plaintext
    tasks.json
    ```

4. **Run the program**:

    ```bash
    python task_manager.py
    ```

## Usage

1. **Manage Tasks**:
   - The program will prompt you to enter new tasks and organize them based on your responses.
   - Specify task descriptions, durations (30 minutes, 1 hour, etc.), and planned dates if applicable.
   - Tasks can be marked for personal attention, delegated to others, or scheduled for later.

2. **Save and Load Tasks**:
   - Tasks are saved to `tasks.json` automatically after each change.
   - When the program is started, it loads tasks from `tasks.json` to continue where you left off.

### Task Categories

- **Inbox**: New tasks.
- **Notes**: Information or tasks that don't require immediate action; reference information.
- **Calendar**: Tasks planned for a specific date.
- **Someday_maybe**: Tasks without a specific timeframe; tasks that can be done someday, not this week.
- **Backlog**: Tasks that require more than two minutes to complete and need to be done this week.
- **Projects**: Vague or complex tasks that need further planning. Note: Complex tasks in this category should later be broken down into simpler tasks and run through the entire task management workflow again.
- **Done**: Completed tasks.
- **Task Delegated**: Tasks assigned to others.

## Code Overview

- `add_task()`: Adds a task to a specified category, with options for duration and date.
- `sort_tasks_by_duration()`: Sorts tasks by duration within a category.
- `sort_calendar_by_date()`: Sorts tasks in the `calendar` by planned date.
- `select_duration()`: Allows the user to choose a task duration from a predefined set.
- `task_management()`: Manages the task sorting workflow with prompts to categorize each new task.

## License

This project is licensed under the MIT License.
