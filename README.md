# Group Playlist Planner

A planned Java terminal application for CS 193 that helps friends choose music together for an occasion.

## Problem

Music sets the mood when friends get together, but the person controlling the playlist often decides what everyone hears. The goal is to make music selection collaborative so the final playlist reflects the group's preferences and gives everyone a chance to contribute.

## Solution and current status

Friends submit songs for an event and anonymously rate other participants' submissions. The program will use song and genre ratings to generate one balanced playlist while giving each friend representation.

The project is currently in the planning stage. Version 1 will run on one shared computer with manually entered songs and local files. Its playlist output will be a saved track list. Spotify API integration, a discovery round for similar songs, and mobile-web support are future improvements; the MVP will not create a playlist in Spotify.

## MVP scope

- Create an event session and register participants.
- Accept song titles, artists, genres, and submitter information, with a submission limit.
- Collect ratings while hiding submitter names during voting and preventing duplicate votes.
- Calculate average song and genre ratings.
- Select highly rated songs to produce a balanced playlist with participant representation.
- Save sessions locally as JSON using Gson.
- Display final results and export the selected songs as a local playlist track list.

The rating scale, submission limit, tie-breaking, treatment of unrated songs, and exact balancing rule will be defined during implementation. Participants take turns on a shared computer; anonymous voting hides names in the interface.

## Future plans

- Spotify API integration to import song information and create playlists, after verifying access and supported features.
- A discovery round for similar-song suggestions.
- Mobile-web support so friends can participate from their phones.
- Additional ideas from the Schedule quadrant: event duration and explicit-content preferences, an energy curve, group vetoes, reusable groups, and a results reveal.

## Tech stack

- **Language:** Java.
- **Interface:** Terminal menu on one shared computer.
- **Java libraries:** Scanner, ArrayList, HashMap, Comparator, java.nio.file, and java.time.
- **External library:** Gson for saving and loading JSON files.
- **Storage:** Local JSON files for sessions, songs, participants, and ratings.
- **Tools:** JDK, Visual Studio Code, Git, and GitHub.
- **Data source:** Manually entered songs. Spotify API integration is planned for a future version.

## Repository structure

```text
src/        Java application source (to be written)
tests/      Planned checks and future test code
docs/       Design document, matrix PDF, diagram image and editable source
data/       Local saved sessions
exports/    Generated playlist track lists
```

Generated session and export files are ignored by Git by default.

## Chunked build plan

Each milestone should end in a meaningful commit. Test each feature as it is implemented.

1. **Set up the project:** Create the GitHub repository, folder structure, VS Code environment, and README.
2. **Build the menu:** Let the user create an event session and register participants.
3. **Add song submissions:** Store song titles, artists, genres, and submitters, including a submission limit.
4. **Implement anonymous rating:** Hide submitter names during voting and prevent duplicate votes.
5. **Calculate results:** Compute average song and genre ratings.
6. **Generate a balanced playlist:** Select highly rated songs from the calculated results while representing participants.
7. **Persistence:** Use Gson to save sessions in JSON format and load saved session data.
8. **Export the playlist:** Display final results and save the selected songs as a local playlist track list.

## Design documents

The completed Eisenhower matrix PDF and student-created system diagram (PNG/JPG and editable source) are pending and will be added under `docs/`.

## Development setup

There is no runnable application yet. Open this folder in VS Code. The selected JDK version, Gson dependency setup, and run instructions will be documented as the application is developed.
