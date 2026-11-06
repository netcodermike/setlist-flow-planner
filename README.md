# Setlist Flow Planner

Order a setlist using tempo and tonal-distance costs, with fixed openers and a transition report.

**Language:** C# · **License:** MIT · **Data:** Local by default

## What it does

- Fixed opener and nearest-transition ordering
- Tempo and circle-of-fifths transition costs
- Readable sequence and validation

## Requirements

.NET 8 SDK.

## Install, validate, and run

```sh
dotnet run -- --self-test
dotnet run -- examples/songs.json
```

Run `--help` where supported, or follow the examples in [docs/usage.md](docs/usage.md). Input files are never overwritten unless explicitly documented.

## Usage and examples

See [docs/usage.md](docs/usage.md) for a walkthrough and [docs/architecture.md](docs/architecture.md) for implementation details. Tests are deterministic and do not require an exchange, paid API, external model, microphone, or private data.

## Boundaries

Greedy heuristic, not a globally optimal setlist. Key must be a circle-of-fifths index 0–11; major/minor mode and musical style are not inferred.

## Privacy

No analytics or accounts are built in. Local file tools process only the paths you supply. For model-server and weather apps, the interface and usage guide identify the destination and the data sent. Do not commit personal input files, model credentials, or generated recordings.

## Development

Run the validation commands above before submitting changes. GitHub Actions runs these checks on pushes and pull requests. See the workflow for the reproducible toolchain. A successful workflow verifies the tested paths; manual audio-device behavior is documented separately.
