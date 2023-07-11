# my-lit-llama
How to run lit-llama

## Commands:

### Clone the repo:

```
git clone https://github.com/Lightning-AI/lit-llama
cd lit-llama
```
### Install the requirements:

```
pip install -r requirements.txt
```

### Download llama weights data:

```
python scripts/download.py --repo_id openlm-research/open_llama_7b --local_dir checkpoints/open-llama/7B
```
### Install SciPy
```
 pip install scipy 

```

### To execute the chatbot in 8bit mode:

```
python generate.py --quantize llm.int8 --prompt "Hello, my name is"
```
### Create links

```
ln -s /home/mostafa/programming/models/llama/pyllama_data/7B/consolidated.00.pth checkpoints/lit-llama/7B/lit-llama.pth
```
```
ln -s /home/mostafa/programming/models/llama/pyllama_data/tokenizer.model checkpoints/lit-llama/tokenizer.model
```
