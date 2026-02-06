# RC Network Builder

Small Flask app that renders thermal RC network diagrams (Foster or Cauer) as SVG.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

The server runs at `http://127.0.0.1:5000`.

## URLs

- `http://127.0.0.1:5000/?type=cauer&order=5`
- `http://127.0.0.1:5000/diagram?type=foster&order=3`
- `http://127.0.0.1:5000/diagram?type=cauer&order=4&labels=on`
- `http://127.0.0.1:5000/embed?type=foster&order=4`

## Notes

- `/diagram` returns SVG with `Content-Type: image/svg+xml`.
- Valid `type` values: `foster`, `cauer`.
- Valid `order`: integer 1..50.
