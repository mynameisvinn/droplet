# DropletML
**DropletML** lets you save and share PyTorch model weights with zero code overhead and no size limitations.

## Install
```bash
pip install DropletML
```

## Quickstart
You can save PyTorch models to a shared store in the same manner you would save to a local filesystem.
```python
from DropletML import droplet

path = droplet('foobar')  # name your droplet
torch.save(model, path)  # identical to saving a model to local file
# prints rainpuddle/foobar-89ea455e.pt
```
Afterwards, anyone with your tag can access your model.
```python
path = droplet('rainpuddle/foobar-89ea455e.pt')
restored_model = torch.load(path)
```