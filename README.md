# my-lit-llama
How to run lit-llama

### Commands:

```
git clone https://github.com/Lightning-AI/lit-llama
cd lit-llama
```
```
pip install -r requirements.txt
```

### To download llama weights data:

```python scripts/download.py --repo_id openlm-research/open_llama_7b --local_dir checkpoints/open-llama/7B```
```


```
python generate.py --quantize llm.int8 --prompt "Hello, my name is"
```
