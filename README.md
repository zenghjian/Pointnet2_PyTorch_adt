Pointnet2/Pointnet++ PyTorch
============================

### Installation

requires python 3.9
`
```bash
pip install -r requirements.txt
pip install -e .
```

### Troubleshooting

- `TypeError: can only concatenate tuple (not "list") to tuple` in `[PATH-TO-VENV]/lib/python3.9/site-packages/pointnet2_ops/pointnet2_modules.py`
`

  use `interpolated_feats = known_feats.repeat(1, 1, unknown.shape[1])` instead of `interpolated_feats = known_feats.expand( *(known_feats.size()[0:2] + [unknown.size(1)]) )`


