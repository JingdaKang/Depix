# Depix

An image-processing tool that attempts to recover text from pixelated screenshots made with a linear box filter. It matches pixel blocks against a search image rendered in the same font/style.

Full original guide: [README.upstream.md](README.upstream.md).

## Requirements

Python 3 and Pillow.

## Getting started

```sh
python -m venv .venv
# Activate .venv, then:
python -m pip install -r requirements.txt
python depix.py -p images/testimages/testimage3_pixels.png -s images/searchimages/debruinseq_notepad_Windows10_closeAndSpaced.png -o output.png
```

## Project structure

| Path | Purpose |
| --- | --- |
| `depix.py` | Command-line entry point |
| `depixlib` | Matching and reconstruction logic |
| `images/testimages` | Example inputs |
| `images/searchimages` | Search images |
| `docs` | Explanation and example output |

## Configuration and limitations

Crop pixelated blocks to one rectangle and supply a search image using the expected font and rendering. Recovery depends on matching assumptions and is not guaranteed for arbitrary redaction. Use the tool only on images you are authorized to analyze.

## Development and validation

The documented example completed during cloud onboarding and produced a decodable 205 × 15 PNG. This demonstrates the example workflow, not exact recovery for arbitrary images.

## Related projects and attribution

Original project and research: [beurtschipper/Depix](https://github.com/beurtschipper/Depix). The preserved upstream README contains the algorithm explanation and article link.

## License

See [LICENSE](LICENSE).
