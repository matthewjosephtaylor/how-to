
# KanDown: A Simple Markdown-Based Task Management System

KanDown is a lightweight, markdown-based task management system that mirrors a Kanban board's workflow. It leverages a simple directory structure to track tasks through their various stages, offering an easy and flexible way to organize, update, and reference tasks. This system avoids the complexities of custom tools and software, allowing users to focus on managing their projects seamlessly.

## Motivations
- **Simplicity:** Provides a straightforward way to manage tasks using only markdown files and directories.
- **Flexibility:** Allows for detailed notes and task descriptions without strict naming or formatting conventions.
- **Compatibility:** Uses snake_case and lowercase for directory names to ensure compatibility across all filesystems.
- **Transparency:** Enables clear tracking of task progress by moving files between directories.
- **Future-Proof:** Designed to work well with both individual use and future team collaborations, potentially automating with AI down the line.

## Directory Structure
KanDown organizes tasks into directories that represent different stages of work. Each task is a markdown file that moves between directories as it progresses:

1. **`backlog/`** – Stores ideas and potential tasks that are not yet prioritized. This is where you capture all incoming ideas and projects.
2. **`ready/`** – Contains tasks that are ready to be worked on. Once you decide that a task is actionable, move its markdown file here.
3. **`in_progress/`** – Houses tasks currently being actively worked on. Moving a task file here indicates it is in progress.
4. **`review/`** – Holds tasks that have been completed but need to be reviewed, tested, or require feedback before they can be finalized.
5. **`blocked/`** – Stores tasks that are temporarily paused or waiting on an external dependency. Use this directory to track issues causing delays.
6. **`done/`** – Contains all completed tasks. Moving a file here signifies that the task is fully finished.
7. **`archive/`** – Keeps older, completed tasks for reference. After tasks have been in `done/` for a while, they can be moved here to keep the system tidy.

## Creating and Managing Tasks
- **Task Creation:** To create a new task, simply create a markdown file in the `backlog/` directory. The file name can be anything descriptive (e.g., `create_initial_ui.md`). There are no strict naming conventions, so make it easy to understand and identify.
- **Task File Format:** Each task file can contain:
  ```markdown
  # Task: Create Initial UI

  **Status:** ready

  **Description:** Design and implement the basic UI layout for the main dashboard.

  **Notes:**
  - Focus on minimalistic design.
  - Add placeholder elements for future functionalities.

  **Subtasks:**
  - [ ] Create wireframe layout.
  - [ ] Implement React components.
  ```
  - **Status:** Can be updated to reflect the task’s current state (e.g., "in_progress", "review").
  - **Notes:** Add any relevant details, updates, or discussions related to the task.
  - **Subtasks:** Include checkboxes for smaller steps within the task.

## Moving Tasks Between Stages
- When the status of a task changes (e.g., from `ready` to `in_progress`), **move the task file** to the corresponding directory. This mirrors how items move through a Kanban board.
  - Example: Move `ready/create_initial_ui.md` to `in_progress/create_initial_ui.md` when work begins.
- **Completion:** When a task is complete, move the file to the `done/` directory. After some time, transfer it to `archive/` for long-term storage.

## Overview and Navigation
- To get an overview of the project status, navigate to the `project-tasks/` directory. Inside each stage's directory, you'll find all the tasks within that phase.
- You can create an optional `index.md` file in the `project-tasks/` root directory to list all tasks and their locations if you prefer a high-level view.

## Benefits of Using KanDown
- **Composability:** Tasks are broken into individual files that are easy to update and move between stages.
- **Transparency:** A clear, visual representation of the project's status through the directory structure.
- **Ease of Use:** No strict file naming rules; just move files to manage progress.
- **Scalable:** Works for personal projects and can easily expand to team use in the future.

KanDown gives you a straightforward, frictionless way to manage tasks without needing specialized software. By leveraging markdown and simple directory movements, you maintain a clear picture of your project's progress.
