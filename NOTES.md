### Notes

- Ubuntu 24.04
- python3.8 `uv venv --python 3.8`
- `python -mpip install -r requirements.txt`
- has trouble with `vi3o` when running `python soccersegcal/dataloader.py`, reason due to incompatible with PIL.Image resize (perhaps old Python?) - pinning it to `vi3o[full]` works
- added `python_dotenv` so we dont' have to modify datasetpath 
- Have some errors running `python soccersegcal/train.py` but Copilot can fix it (see commit)
- Run `mlflow ui` to monitor Training progress

#### Pytorch3d

- Has to build from source
- Has to install Cuda toolkit so it can be built with GPU support (Cuda 12.6, as Torch was install with 12.6 wheel)
- After that can run `python soccersegcal/estimate_cameras.py -c mlruns/785205517016288233/c1a7813fd0d84837acc77aa3ecccaf31/checkpoints/last.ckpt -i \[1,2,3,4,5\] -s` success fully

### Using uv

```bash
uv venv --python 3.9
uv pip install -r requirements.txt
uv pip install -e .
uv pip install --no-build-isolation "git+https://github.com/facebookresearch/pytorch3d.git@stable"
```