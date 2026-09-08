# notevectors

Tiny embedding search: numpy cosine over cached vectors

Side project, maintained when I have time.

## Usage

```bash
python search.py ./notes
>> how do I back up my database?
```

## What it does

- Interactive REPL and one-shot modes
- Vectors cached to .npy so re-runs are instant
- Reranks by recency when scores tie
- sentence-transformers when available, TF-IDF fallback

## Install

```bash
pip install -r requirements.txt
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── development.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── requirements.txt
└── search.py
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```
