<img src="./gateloop.png" width="450px"></img>

## GateLoop Transformer (wip)
<a href="https://arxiv.org/abs/2311.01927">GateLoop</a>

### Install

```bash
$ pip install gateloop-transformer
```

### Usage

```python
import torch
from gateloop_transformer import Transformer

model = Transformer(
    num_tokens = 256,
    dim = 624,
    depth = 6,
    use_gate_looped_attn = True
)

ids = torch.randint(0, 256, (1, 1024))
logits = model(ids) # (1, 1024, 256)
```

### Character-level Language Modeling

Install requirements

```bash
$ pip install -r requirements.txt
```

Then run the `train.py` script for autoregressive modeling on enwik8

```bash
$ python train.py
```

## Citations

```bibtex
@inproceedings{Katsch2023GateLoopFD,
    title   = {GateLoop: Fully Data-Controlled Linear Recurrence for Sequence Modeling},
    author  = {Tobias Katsch},
    year    = {2023},
    url     = {https://api.semanticscholar.org/CorpusID:265018962}
}
```
