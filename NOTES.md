### Notes

- Ubuntu 24.04
- python3.8 `uv venv --python 3.8`
- `python -mpip install -r requirements.txt`
- has trouble with `vi3o` when running `python soccersegcal/dataloader.py`, reason due to incompatible with PIL.Image resize (perhaps old Python?) - pinning it to `vi3o[full]` works
- added `python_dotenv` so we dont' have to modify datasetpath 
- Have some errors running `python soccersegcal/train.py` but Copilot can fix it (see commit)
- Run `mlflow ui` to monitor Training progress

### Additional commands (missing in requirements.txt)

```bash
python -mpip install torchvision
python -mpip install pyglet
```