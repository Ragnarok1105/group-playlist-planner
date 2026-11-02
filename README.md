# Group Playlist Planner

A Java project for CS 193 that lets friends put together a playlist for a hangout, party, or other event.

## Problem

Whenever my friends and I get together, music is a big part of it. Usually, whoever has the aux ends up choosing what everyone listens to. I want to give everyone a say and put together a playlist that fits the occasion.

## Solution and current status

Everyone submits a few songs and takes turns rating the other submissions without seeing who picked them. The program uses those ratings to find the group's favorite songs and genres, then puts together a playlist that gives each friend some representation.

I'm starting with a terminal program on one shared computer. People will enter songs manually, and the program will save the final track list to a file. Connecting it to Spotify, suggesting similar songs, and letting people join from their phones are things I want to add later.

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

- [Interface mockup draft](docs/CS193_Final.drawio): my editable draw.io file showing the welcome, event setup, song submission, and results screens.
- The system diagram still needs labeled connections, a clear entry point, and the remaining MVP steps before it is ready for submission.
- The completed Eisenhower matrix PDF and exported diagram image will be added here once ready.

## Development setup

There is no runnable application yet. Open this folder in VS Code. The selected JDK version, Gson dependency setup, and run instructions will be documented as the application is developed.
