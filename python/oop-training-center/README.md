# Smart Training Center Management System

A console-based system for managing a training center — trainees, course enrollment, attendance, scoring, certificate eligibility, and reporting — built around three cooperating classes: `Trainee`, `Course`, and `TrainingCenter`.

`TrainingCenter` composes the other two to orchestrate everything, and every entry point validates its data (names, emails, scores, course codes) before it touches state, so bad data never quietly slips in.

## Core Features

- Registration & enrollment with duplicate/capacity checks via custom exceptions
- Attendance tracking (sets prevent duplicate session records) and score recording
- NumPy-driven course analytics — mean, min, max, std dev, boolean filtering
- Automatic status (`Passed` / `Failed` / `Incomplete`) and certificate eligibility logic
- Trainee, course, and center-wide reports
- JSON save/reload and CSV export
- Menu-driven console interface, plus a 15-case test suite

## Skills & Concepts Demonstrated

- OOP design — encapsulation, composition, `to_dict()`/`from_dict()` serialization
- Custom exception hierarchies for domain-specific error handling
- Deliberate data structure choices — sets, tuples, and dicts picked for what each constraint actually needs
- Validation-first design — every entry point normalizes and checks input before it touches state
- NumPy for aggregate statistics and boolean masking
- File I/O — JSON round-tripping, CSV generation
- Test-driven verification of both expected successes and expected failures

## Tech Stack

`Python 3` · `NumPy` · `json` · `csv` · `pathlib`

## Sample Output

Running end-to-end on the sample dataset (3 courses, 5 trainees):

```text
Training Center: Future Skills Training Center
Courses: 4
Registered trainees: 5
Total enrollments: 8
Passed records: 2
Failed records: 1
Incomplete records: 5
Certificates eligible: 1
Top course: Python Fundamentals
```

All 15 test cases pass, covering registration, enrollment limits, score boundaries, all three completion statuses, and JSON/CSV persistence.

## How to Run

Open the notebook and run all cells top to bottom. The menu-driven interface is defined but not auto-launched (for clean automated testing) — call `run_menu(center)` in a new cell to try it interactively.
