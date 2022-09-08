# Template documentation repository

This repository is a template allowing easy creation of python repository with a full documnentation automatisation.

## Usage

You can rename the `src` folder to whichever name you want for your source code (library name if it is a library)

Once done you need to replace `src` to your new name in the following files :
- `scripts/generate_index.py`
- `scripts/generate_references.py`
- `.github/workflows/generate_gh_pages.yml`
- `.github/workflows/tag_latest_release_gh_pages.yml`

## First set-up

Once you have set up everything you can do the following commands :
```bash
python -m venv venv
source venv/bin/activate
pip install -e .
mike deploy [version] latest
mike set-default latest
```

All those commands will build a first version `[version]` of your doc, tag it as the latest and use it by default.
You can then do the following command to check it locally :

```bash
mike serve
```