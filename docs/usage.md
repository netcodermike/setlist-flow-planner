# Using Setlist Flow Planner

## Quick start

Create a JSON array with `title`, `bpm`, and `key` (circle-of-fifths index, e.g. C=0, G=1, D=2). Run `dotnet run -- examples/songs.json`. The first input stays the opener.

## Supported workflow

1. Fixed opener and nearest-transition ordering.
2. Tempo and circle-of-fifths transition costs.
3. Readable sequence and validation.

## Validation and troubleshooting

Run the commands in the README. Invalid inputs produce explicit errors rather than silently changing the requested operation. Browser audio requires a user gesture; microphone apps require HTTPS or localhost and permission. For file tools, supply supported input formats and writable output directories.

## Limitations

Greedy heuristic, not a globally optimal setlist. Key must be a circle-of-fifths index 0–11; major/minor mode and musical style are not inferred.

Tests use synthetic fixtures. These tests do not certify hardware compatibility, real-world forecast quality, trained-model accuracy, or production suitability for every input.
