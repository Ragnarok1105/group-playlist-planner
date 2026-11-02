# Group Playlist Planner

A Java terminal application planned for CS 193 that helps friends choose music together for an event.

## Project goal

Choosing music for a group event can leave one person's taste in control. This project will let friends submit songs and anonymously rate one another's choices, then generate a track list that reflects group preferences while giving participants representation.

## Current status

Planning and repository setup. The application is not implemented yet. The first version will run on one shared computer; it will generate a track list rather than play audio or create a Spotify playlist.

## MVP scope

- Create an event session and register participants.
- Accept a limited number of song submissions per participant, including title, artist, genre, and an optional Spotify link.
- Hide submitter names during rating; reject self-ratings, duplicate votes, and invalid input. Anonymity is a shared-screen convention, not a security guarantee.
- Calculate average song and genre ratings, with defined behavior for ties and unrated songs.
- Select highly rated tracks while giving each participant representation when playlist capacity allows.
- Save and reload sessions as JSON and export the final track list as plain text.

Rating scale, submission limits, tie-breaking, duplicate-song handling, and the exact selection rule will be specified and tested during development.

## Future plans

- Spotify playlist import and export, after checking API access and supported features.
- A discovery round in which participants vote on similar-song suggestions.
- Live rooms that participants join from separate phones.
- Event duration, explicit-content preferences, and manually tagged energy curves.
- Group vetoes, reusable groups, and a results reveal with crowd favorites and divisive songs.

## Tech stack

- **Language:** Java.
- **Interface:** Terminal menus on one shared computer.
- **Standard library:** Scanner, ArrayList, HashMap, Comparator, java.nio.file, and java.time.
- **External library:** Gson for JSON serialization and deserialization.
- **Storage:** Local JSON session files and plain text playlist exports.
- **Tools:** JDK, Visual Studio Code with the Extension Pack for Java, Git, and GitHub.
- **Data source:** Manual song entry. No external API or Spotify account is required for the MVP.

## Repository structure

```text
src/        Java application source (to be written)
tests/      Test scenarios and future test code
docs/       Design document, Eisenhower matrix, diagram image and editable source
data/       Local saved sessions (ignored except this folder's README)
exports/    Generated track lists (ignored except this folder's README)
```

## Development milestones

Each milestone should end in a meaningful commit as the work is completed.

1. Set up the repository, Java folder structure, VS Code environment, and initial README.
2. Build event-session menus, participant registration, and input validation.
3. Add song submissions and enforce a per-participant limit.
4. Implement anonymous rating, self-rating prevention, and duplicate-vote checks.
5. Calculate song and genre averages and handle ties and unrated songs.
6. Generate a balanced playlist with participant representation when capacity allows.
7. Save and reload complete sessions using Gson and JSON.
8. Display results and export a plain text track list.
9. Test the complete workflow, fix issues, and document setup and usage.

## Design documents

The completed Eisenhower matrix PDF and the student-created system diagram (PNG and editable source) are pending and will be added under `docs/`. The design document will link to this repository.

## Running the project

There is no runnable application yet. Build instructions, the selected JDK version, and dependency setup will be added when the Java environment is configured. Open this folder in VS Code to begin development.
