# LoRA testing - Low Rank Adaptation

## Setup
### 1. Download a model (optional for testing without your lora)
Download local ollama installer https://ollama.com/download

in terminal:
```bash
ollama pull tinyllama
```
```bash
ollama run tinyllama
```
then you can test it with some prompt
```text
Explain quantum computing in one sentence.
```

### 2. Fine-tuning

#### A. Curated dataset
Either download a dataset from:

https://huggingface.co/datasets/

or you could create your own with a .jsonl in the following format:
```json
{"instruction": "What is TrailTracker?", "output": "TrailTracker is a webapp for planning and tracking your hikes."}
```
or a slightly more advanced format like:
```json
{"instruction": "What is the main feature of TrailTracker?", "context": "Webapp for hike planning", "output": "The main feature of TrailTracker is to plan hikes and track progress."}
```

#### B. Create a venv
Make sure you create the venv with python 3.12 or earlier versions.

https://pytorch.org/get-started/locally/ to get the command to install libraries. OS, CUDA or CPU...

ex windows with rtx 3070 gpu: 
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
and general packages:
```bash
pip install transformers datasets peft accelerate bitsandbytes jupyter ipykernel
```
```bash
pip install scipy sentencepiece
```

#### C. Run training notebook(s)
Setup the training.ipynb or training_advanced.ipynb depending on dataset format used. 
