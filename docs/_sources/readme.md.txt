# Lightning + Colossal-AI

**Efficient Large-Scale Distributed Training with [Colossal-AI](https://colossalai.org/) and [Lightning AI](https://lightning.ai)**












______________________________________________________________________

## Installation

```bash
pip install -U lightning lightning-colossalai
```

## Usage

Simply set the strategy argument in the Trainer:

```py
import lightning as L

trainer = L.Trainer(strategy="colossalai", precision="16-mixed", devices=...)
```

For more fine-grained tuning of Colossal-AI's parameters, pass the strategy object to the Trainer:

```py
import lightning as L
from lightning_colossalai import ColossalAIStrategy

strategy = ColossalAIStrategy(...)
trainer = L.Trainer(strategy=strategy, precision="16-mixed", devices=...)
```

Find all configuration options [in the docs](https://pytorch-lightning.readthedocs.io/en/latest/advanced/third_party/colossalai.html)!
